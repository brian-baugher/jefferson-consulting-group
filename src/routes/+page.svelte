<script>
    import background from '$lib/assets/uva_rotunda_dome.jpg';
    import InfoSection from '$lib/InfoSection.svelte';
    import cavman from '$lib/assets/cavman.jpg'
    import jpj from '$lib/assets/jpj.jpg'
    let width = 0;
    $: mobile = width < 850;
</script>

<svelte:window bind:innerWidth={width} />

<div class="landing" style="background-image: url({background});">
<h1>Jefferson Consulting Group</h1>
<p>Virginia's leading consultants</p>
<button>Join today</button>
</div>
<div class="banner left-image" class:mobile><InfoSection {mobile} picture={cavman} title='Title' text='Mollit anim commodo laboris officia reprehenderit id cupidatat eiusmod ad ad enim. Dolor id exercitation magna occaecat sit mollit ad eu aliqua sint. Commodo culpa veniam occaecat officia ullamco amet velit dolor laborum proident commodo officia ullamco. Fugiat consequat commodo ut labore voluptate duis ex dolor deserunt dolore irure. Non do exercitation elit duis deserunt mollit.'/></div>
<div class="banner right-image" class:mobile><InfoSection right {mobile} picture={jpj} title='Title' text='Nostrud ut sit exercitation incididunt est dolor ullamco amet eu quis. Laborum labore duis qui ea aute consectetur labore elit aute ex consectetur in occaecat. Officia nulla proident esse do dolor nisi excepteur. Exercitation deserunt consectetur veniam voluptate consequat nisi ea laborum reprehenderit occaecat nulla. Aliqua cupidatat ea elit id proident in velit adipisicing. Officia reprehenderit cupidatat nostrud Lorem eiusmod.' /> </div>

<style>
    .banner{
        width: 100%;
        height: 110vh;
        box-sizing: border-box;
        background-color: black;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        display: flex;
        align-items: center;
    }
    .left-image{
        padding-right: 40%;
    }
    .right-image{
        padding-left: 40%;
    }
    .mobile{
        padding: 0;
    }
    button{
        border: solid lightblue .2vmin;
        padding: 2vmin;
        font-size: 4cqmin;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        background-color: transparent;
        color: white;
        z-index: 1;
    }
    h1{
        font-size: 10cqmin;
        font-weight: 300;
    }
    p, h1{
        margin: 0;
        padding: 0;
        color: white;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        z-index: 1;
        text-align: center;
    }
    p{
        font-weight: 100;
        text-align: center;
    }
    .landing{
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
        position: relative;
        background-size: cover;
        flex-direction: column;
        gap: 5%;
        width: 100%;
        background-position: center;
        max-width: 100%;
        overflow: auto;
        min-width: 100%;
    }
    .landing::before {
        content: "";
        position: absolute;
        top: 0px;
        right: 0px;
        bottom: 0px;
        left: 0px;
        background-color: rgba(0,0,0,0.40);
    }
</style>