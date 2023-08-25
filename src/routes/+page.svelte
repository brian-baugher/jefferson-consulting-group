<script lang="ts">
	import background from '$lib/assets/uva_rotunda_dome.jpg';
	import InfoSection from '$lib/InfoSection.svelte';
	import cavman from '$lib/assets/cavman.jpg';
	import jpj from '$lib/assets/jpj.jpg';

	let width = 0;
	$: mobile = width < 850;
</script>

<svelte:window bind:innerWidth={width} />

<div class="landing" style="background-image: url({background});">
	<h1>Jefferson Consulting Group</h1>
	<p>Virginia's leading consultants</p>
	<button><a target="_blank" href="https://forms.gle/EMuD4AZRYrLfSikL9">Join today</a></button>
</div>
<div class="banner left-image" class:mobile>
	<InfoSection
		{mobile}
		picture={cavman}
		title="Title"
		text="Mollit anim commodo laboris officia reprehenderit id cupidatat eiusmod ad ad enim. Dolor id exercitation magna occaecat sit mollit ad eu aliqua sint. Commodo culpa veniam occaecat officia ullamco amet velit dolor laborum proident commodo officia ullamco. Fugiat consequat commodo ut labore voluptate duis ex dolor deserunt dolore irure. Non do exercitation elit duis deserunt mollit."
	/>
</div>
<div class="banner right-image" class:mobile>
	<InfoSection
		right
		{mobile}
		picture={jpj}
		title="Title"
		text="Nostrud ut sit exercitation incididunt est dolor ullamco amet eu quis. Laborum labore duis qui ea aute consectetur labore elit aute ex consectetur in occaecat. Officia nulla proident esse do dolor nisi excepteur. Exercitation deserunt consectetur veniam voluptate consequat nisi ea laborum reprehenderit occaecat nulla. Aliqua cupidatat ea elit id proident in velit adipisicing. Officia reprehenderit cupidatat nostrud Lorem eiusmod."
	/>
</div>

<style>
	.mobile {
		padding: 0;
	}
	button {
		border: solid lightblue 0.2vmin;
		padding: 2vmin;
		font-size: 4cqmin;
		font-family: Roboto, 'serif';
		background-color: transparent;
		color: white;
		z-index: 1;
	}
	button > a {
		color: inherit;
		text-decoration: none;
	}
</style>
