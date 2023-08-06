<script>
	// place files you want to import through the `$lib` alias in this folder.
	import { browser } from '$app/environment';
	import { goto } from '$app/navigation';
	import logo from '$lib/assets/globe-4-64.png';
	import MdMoreHoriz from 'svelte-icons/md/MdMoreHoriz.svelte';
	/** @type {string}*/
	let currentPage;
	let b = browser;
	$: if (b) {
		currentPage = window.location.pathname;
	}

	let width = 0; // less then 850 collapse
	$: console.log(width);
	$: smallPage = width < 850;
	$: showDropdown = false && smallPage;

	let scrollY = 0; //over 100 switch bkgrnd
	$: console.log(scrollY);
	$: scrolledDown = scrollY >= 100;

	const links = [
		{ path: '/about', name: 'About' },
		{ path: '/projects', name: 'Projects' },
		{ path: '/leadership', name: 'Leadership' },
		{ path: '/careers', name: 'Careers' }
	];
</script>

<svelte:window bind:innerWidth={width} bind:scrollY />

<div class="nav" class:black-background={scrolledDown || showDropdown}>
	<button
		on:click={() => {
			showDropdown = false;
			goto('/');
			currentPage = '/';
		}}><img src={logo} alt="logo" class:current={currentPage === '/'} /></button
	>

	<div class="links" class:hide={smallPage}>
		{#each links as link}
			<a
				href={link.path}
				on:click={() => (currentPage = link.path)}
				class:current={currentPage === link.path}>{link.name}</a
			>
		{/each}
	</div>
	<button
		class="dropdown-btn"
		on:click={() => (showDropdown = !showDropdown)}
		class:hide={!smallPage}><MdMoreHoriz /></button
	>
</div>

<div
	class="dropdown"
	class:invis={!showDropdown}
	class:black-background={scrolledDown || showDropdown}
>
	{#each links as link}
		<a
			href={link.path}
			on:click={() => {
				showDropdown = false;
				currentPage = link.path;
			}}
			class:current={currentPage === link.path}>{link.name}</a
		>
	{/each}
</div>

<style>
	.invis {
		visibility: hidden;
		opacity: 0 !important;
		pointer-events: none;
		transform: translateY(-35%);
	}
	.nav {
		display: flex;
		padding: 0 25vw;
		margin: 0%;
		height: 5vh;
		width: 100%;
		box-sizing: border-box;
		align-items: center;
		background-color: transparent;
		font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial,
			sans-serif;
		font-size: 3cqmin;
		position: fixed;
		z-index: 2;
	}
	a {
		text-decoration: none;
		color: lightgray;
	}

	.dropdown {
		display: flex;
		flex-direction: column;
		background-color: transparent;
		position: fixed;
		z-index: 2;
		top: 5vh;
		padding: 1vh 25vw;
		gap: 1cqh;
		width: 100%;
		visibility: visible;
		opacity: 1;
	}
	a:hover {
		color: white;
	}
	.links {
		display: flex;
		gap: 10%;
	}
	.current {
		color: white;
	}
	button {
		margin: 0;
		padding: 0;
		background: none;
		border: none;
		margin-right: auto;
		height: 100%;
		display: flex;
		flex: none;
		overflow: hidden;
		align-items: center;
		color: lightgray;
		font-size: 3cqmin;
	}
	.dropdown-btn {
		margin-left: auto;
		margin-right: 0;
	}
	img {
		color: lightgray;
		flex: 1;
		height: 4cqh;
	}
	.hide {
		display: none;
	}
	.black-background {
		background: black;
		transition: 0.5s all ease;
	}
	button:hover {
		color: white;
	}
</style>
