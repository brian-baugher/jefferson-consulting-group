<script lang="ts">
	import InfoBox from '$lib/InfoBox.svelte';
	import InfoSection from '$lib/InfoSection.svelte';
	import lecture from '$lib/assets/lecture.jpg';
	import memorial from '$lib/assets/memorial.jpg';
	import hilton from '$lib/assets/hilton.jpg';
	import company from '$lib/assets/company.jpg';

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
		<p class="info">To drive measurable impact through curiosity, growth, and sustainability</p>
	</InfoBox>
</div>
<div class="banner left-image" class:mobile>
	<InfoSection
		title="Why JCG?"
		text="For companies seeking to support future business leaders while gaining invaluable insights through an unique opportunity, our teams are the perfect match for you. We are a trusted partner bringing a fresh perspective, data-driven insights, and actionable strategies to drive tangible results and sustainable growth in an ever-evolving business landscape."
		picture={lecture}
		{mobile}
	/>
</div>
<div class="banner" class:mobile>
	<InfoBox {mobile}>
		<h1 class="info" class:mobile>Our Fall 2023 Clients</h1>
		<!--add a wraper div when we add more logos-->
		<div class="sponsor-container">
			<div class="hilton sponsor-row" class:mobile>
				<a href="https://www.hilton.com/en/" target="_blank">
					<img class="info" src={hilton} alt="hilton" />
				</a>
				<p class="info small">
					Excepteur eiusmod anim incididunt enim occaecat cillum nulla consectetur incididunt
					pariatur ullamco irure velit. Incididunt proident eiusmod exercitation ullamco labore id
					dolor in fugiat. Minim et dolor mollit eu ipsum laboris mollit fugiat Lorem ad. Laboris ut
					mollit mollit reprehenderit consectetur eu cillum in. Eiusmod labore magna est esse quis.
				</p>
			</div>
			<div class="sponsor-row" class:mobile>
				<a href="https://www.google.com/" target="_blank">
					<img class="info" src={company} alt="company" />
				</a>
				<p class="info small">
					Dolore officia tempor occaecat eiusmod sint duis amet. Ex deserunt minim ut laboris.
					Excepteur laborum fugiat id elit exercitation. Aliquip est laborum culpa mollit consequat
					sit dolor consequat minim minim. Sit culpa ipsum laboris culpa pariatur aliquip esse.
					Mollit cupidatat non adipisicing id aliquip pariatur.
				</p>
			</div>
			<div class="sponsor-row" class:mobile>
				<a href="https://www.google.com/" target="_blank">
					<img class="info" src={company} alt="company" />
				</a>
				<p class="info small">
					Dolore officia tempor occaecat eiusmod sint duis amet. Ex deserunt minim ut laboris.
					Excepteur laborum fugiat id elit exercitation. Aliquip est laborum culpa mollit consequat
					sit dolor consequat minim minim. Sit culpa ipsum laboris culpa pariatur aliquip esse.
					Mollit cupidatat non adipisicing id aliquip pariatur.
				</p>
			</div>
		</div>
	</InfoBox>
</div>
<div class="banner" class:mobile>
	<form name="contact" method="POST" netlify>
		<div class="big-boy column-container">
			<div class='row'>
				<h1>Contact Us</h1>
			</div>
			<div class="row">
				<div class="column-container">
					<div class="field">
						<input type="text" placeholder="Thomas Jefferson" name="name" />
					</div>
					<div class="field">
						<input type="email" placeholder="tj@virginia.edu" name="email" />
					</div>
					<button class='send' type="submit">Send</button>
				</div>
				<div class="big-container">
					<textarea name="message" placeholder="I want to learn more about JCG!" />
				</div>
			</div>
		</div>
	</form>
</div>

<style>
	.send{
		height: 38cqh;
		width: 30cqw;
		border-radius: 10px;
		font-size: xx-large;
		background-color: var(--orange);
		box-shadow: none;
		border: solid 2px white;
	}
	textarea, input{
		background: none;
		border: solid white 2px;
		border-radius: 10px;
		color: white;
	}
	input{
		height: 10cqh;
		width: 30cqw;
	}
	textarea{
		height: 62cqh;
		width: 60cqw;
	}
	form {
		height: 100cqh;
		width: 100cqw;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	form div.column-container {
		width: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		gap: 10px;
	}
	.big-boy{
		flex: 1;
	}
	.row{
		display: flex;
		gap: 10px;
	}
	h1.mobile {
		font-size: 5cqh !important;
	}
	.sponsor-container {
		display: flex;
		flex-direction: column;
		gap: 2vh;
	}
	.sponsor-row {
		display: flex;
		align-items: center;
		gap: 10%;
	}
	.mobile.sponsor-row {
		flex-direction: column;
	}
	.mobile.sponsor-row img {
		height: 25cqh;
		width: 25cqh;
	}
	.mobile.sponsor-row p {
		font-size: 2cqh !important;
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

	h1.info {
		font-size: 5cqmin;
	}
	p.info {
		font-size: 3cqmin;
		text-align: center;
	}
	img.info {
		height: 17vmin;
		width: 17vmin;
	}
	.small {
		font-size: 2cqmin !important;
	}
	.sponsor-row > a {
		border: none;
		margin: 0;
		padding: 0;
		height: fit-content;
		width: fit-content;
		box-sizing: border-box;
		align-items: center;
		display: flex;
		transition: 0.5s all ease;
	}

	.sponsor-row > a:hover {
		transform: scale(110%);
	}
</style>
