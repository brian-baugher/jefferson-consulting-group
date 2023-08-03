<script>
    import background from '$lib/assets/uva_rotunda_dome.jpg'
</script>

<div class="landing" style="background-image: url({background});">
<h1>Jefferson Consulting Group</h1>
<p>Virginia's leading consultants</p>
</div>


<style>
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
        width: 100vw;
        background-position: center;
        max-width: 100%;
        overflow: hidden;
        min-width: 100vw;
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