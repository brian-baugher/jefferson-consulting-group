<script>
	export let mobile = false;
</script>

<div class="info" class:mobile>
	<slot />
</div>

<style>
	div.mobile{
		width: 95%;
		height: 95%;
	}
	.info {
		width: 60%;
		height: 70%;
		box-sizing: border-box;
		border-bottom: double lightblue 4vh;
		border-top: double lightblue 4vh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		padding: 3%;
	}
</style>
