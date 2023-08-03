<script>
    // place files you want to import through the `$lib` alias in this folder.
    import {browser} from '$app/environment'
    import {goto} from '$app/navigation'
    import logo from '$lib/assets/globe-4-64.png'
    /** @type {string}*/
    let currentPage;
    let b = browser;
    $: if(b){
        currentPage = window.location.pathname;
    }

    let width = 0;
    $: console.log(width)

    let scrollY = 0;
    $: console.log(scrollY)
</script>

<svelte:window bind:innerWidth={width} bind:scrollY={scrollY}/>

<div class="nav">
    <button on:click={() => {goto('/'); currentPage='/'}}><img src={logo} alt="logo" class:current={currentPage==='/'}/></button>
    
    <div class="links">
        <a href="/about" on:click={()=>currentPage='/about'} class:current={currentPage==='/about'}>About</a>
        <a href="/projects" on:click={()=>currentPage='/projects'} class:current={currentPage==='/projects'}>Projects</a>
        <a href="/leadership" on:click={()=>currentPage='/leadership'} class:current={currentPage==='/leadership'}>Leadership</a>
        <a href="/careers" on:click={()=>currentPage='/careers'} class:current={currentPage==='/careers'}>Careers</a>
    </div>
</div>


<style>
    .nav{
        display: flex;
        padding: 0 25vw;
        margin: 0%;
        height: 5vh;
        width: 100%;
        box-sizing: border-box;
        align-items: center;
        background-color: transparent;
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
        font-size: 3cqmin;
        position: absolute;
        z-index: 1;
    }
    a{
        text-decoration: none;
        color: lightgray;
    }
    a:hover{
        color: white;
    }
    .links{
        display: flex;
        gap: 10%;
    }
    .current{
        color: white;
    }
    button{
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
    }
    img{
        color: lightgray;
        flex: 1;
        height: 4cqh;
    }
</style>