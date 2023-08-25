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
		title="Who We Are"
		text="Jefferson Consulting Group (JCG) is a pro-bono consulting group founded by students at the University of Virginia's McIntire School of Commerce.
		 JCG is comprised of undergraduate students currently studying at the University of Virginia. Our teams offer a diverse range of backgrounds and work
		 experience/mentorship at top firms within industries ranging from advisory to technology to investment banking."
	/>
</div>
<div class="banner right-image" class:mobile>
	<InfoSection
		right
		{mobile}
		picture={jpj}
		title="Our Philosophy"
		text="Our philosophy and passion revolve around curiosity, growth, sustainability, and driving measurable impact.
		 We fuel our intellectual curiosity and strong problem solving skills into providing innovatice consulting services for our clients."
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
