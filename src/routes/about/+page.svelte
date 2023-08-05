<script>
	import InfoBox from "$lib/InfoBox.svelte";
import InfoSection from "$lib/InfoSection.svelte";
    import lecture from '$lib/assets/lecture.jpg'
    let width = 0;
    $: mobile = width < 850;
</script>

<svelte:window bind:innerWidth={width} />

<div class="about">
    <div class="small-banner"><InfoBox/></div>
</div>
<div class="banner left-image" class:mobile>
    <InfoSection title='Title' text='Exercitation in veniam sint occaecat nostrud in veniam est quis sunt mollit in. Quis amet cillum enim ipsum consectetur adipisicing labore ad laboris sint cupidatat. Aliquip aliqua ipsum dolore eu ex minim tempor laborum excepteur proident deserunt nulla.' picture={lecture} {mobile}/>
</div>

<style>
    .about{
        height: 100vh;
        width: 100%;
        background-color: black;
        margin: 0;
        padding: 0;
        overflow: auto;
        box-sizing: border-box;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .mobile{
        padding: 0;
    }
    .about *{
        color: white;
    }
    .banner {
        color: white;
        justify-content: center;
    }

    .small-banner{
        justify-content: center;
    }
</style>