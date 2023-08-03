<script>
    // place files you want to import through the `$lib` alias in this folder.
    import {browser} from '$app/environment'
    import {goto} from '$app/navigation'
    /** @type {string}*/
    let currentPage;
    let b = browser;
    $: if(b){
        currentPage = window.location.pathname;
    }
</script>

<div class="nav">
    <button on:click={() => {goto('/'); currentPage='/'}}><img alt="logo" class:current={currentPage==='/'}/></button>
    
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
        align-items: center;
        background-color: gray;
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
        font-size: 1.25rem;
        position: sticky;
    }
    a{
        text-decoration: none;
        color: lightgray;
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
    }
    img{
        color: lightgray;
    }
</style>