<script>
	import InfoBox from '$lib/InfoBox.svelte';
	import InfoSection from '$lib/InfoSection.svelte';
	import lecture from '$lib/assets/lecture.jpg';
	import memorial from '$lib/assets/memorial.jpg'
	let width = 0;
	$: mobile = width < 850;
</script>

<svelte:window bind:innerWidth={width} />

<div class="landing" style="background-image: url({memorial});">
	<h1>About Us</h1>
</div>
<div class="small-banner"><InfoBox /></div>
<div class="banner left-image" class:mobile>
	<InfoSection
		title="Title"
		text="Exercitation in veniam sint occaecat nostrud in veniam est quis sunt mollit in. Quis amet cillum enim ipsum consectetur adipisicing labore ad laboris sint cupidatat. Aliquip aliqua ipsum dolore eu ex minim tempor laborum excepteur proident deserunt nulla."
		picture={lecture}
		{mobile}
	/>
</div>

<style>
	h1 {
		font-size: 10cqmin;
		font-weight: 300;
	}
	h1 {
		margin: 0;
		padding: 0;
		color: white;
		font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode',
			Geneva, Verdana, sans-serif;
		z-index: 1;
		text-align: center;
	}
	.mobile {
		padding: 0;
	}
	.banner {
		color: white;
		justify-content: center;
	}

	.small-banner {
		justify-content: center;
		color: white;
	}
</style>
