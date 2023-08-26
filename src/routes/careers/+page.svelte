<script lang="ts">
	import humpback from '$lib/assets/humpback.jpg';

	let width = 0;
	$: mobile = width < 850;
</script>

<svelte:window bind:innerWidth={width} />

<div class="landing" style="background-image: url({humpback})">
	<h1>Careers</h1>
</div>
<div class="small-banner">
	<div class="circle" class:mobile>
		<p>
			Are you passionate about solving real-world business challenges? Seeking to apply your academic knowledge in a practical setting?
			<br/> <br/>
 			<strong>Jefferson Consulting Group is a student-led consulting group where innovative minds collaborate to provide strategic insights and solutions to pressing industry issues.</strong>
		</p>
	</div>
</div>
<div class="small-banner">
	<div class="rounded left" class:mobile>
		<p>
			<strong>Important Dates</strong>
		</p>
		<br/>
	</div>
	<div class="rounded right" class:mobile>
		<p>
			<strong>Interest meetings</strong>
		</p>
		<br/>
		<ul>
			<li>Aug 29: In-Person Orientation<br/>[Time] in [Location]</li>
			<li>Aug 31: Virtual Orientation</li>
			<li>Sept 5: In-Person Orientation<br/>[Time] in [Location]</li>
			<li>Sept 5: In-Person Orientation<br/>[Time] in [Location]</li>
		</ul>
		<small>*must attend at least 1 meet</small>
	</div>
</div>

<style>
	.circle, .rounded{
		background-color: var(--orange);
		margin: 0 auto;
		display: flex;
		align-items: center;
		justify-content: center;
		box-sizing: border-box;
		padding: 5%;
	}
	.circle {
		border-radius: 50%;
		width: 65cqmin;
		height: 65cqmin;
		transform: translateX(-50%);
	}
	div p {
		margin: 0;
		padding: 0;
		text-align: center;
		color: var(--white);
		font-size: 3cqmin;
	}
	.circle.mobile {
		transform: translateX(-25%);
	}
	.rounded{
		border-radius: 30px;
		width: 35cqmin;
		height: 35cqmin;
		flex-direction: column;
		padding: 2%;
	}
	.rounded.right{
		transform: translateY(-50%);
	}
	.rounded p {
		font-size: 2.5cqmin;
	}
	li {
		font-size: 2cqmin;
		color: var(--white);
		margin-bottom: 3%;
	}
	ul {
		margin: 0;
		padding: 0;
	}
	small {
		color: var(--blue);
		font-size: 1.5cqmin;
	}
</style>