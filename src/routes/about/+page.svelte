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
<div class="small-banner">
	<InfoBox>
		<h1 class="info">Our Mission</h1>
		<p class="info">Ex dolor ea consequat ex laborum.</p>
	</InfoBox>	
</div>
<div class="banner left-image" class:mobile>
	<InfoSection
		title="Title"
		text="Exercitation in veniam sint occaecat nostrud in veniam est quis sunt mollit in. Quis amet cillum enim ipsum consectetur adipisicing labore ad laboris sint cupidatat. Aliquip aliqua ipsum dolore eu ex minim tempor laborum excepteur proident deserunt nulla."
		picture={lecture}
		{mobile}
	/>
</div>

<style>
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

	h1.info {
		font-size: 5cqmin;
	}
	p.info {
		font-size: 3cqmin;
	}
</style>
