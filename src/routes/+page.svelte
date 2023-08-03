<script>
    import background from '$lib/assets/uva_rotunda_dome.jpg'
</script>

<div class="landing" style="background-image: url({background});">
<h1>Jefferson Consulting Group</h1>
</div>


<style>
    h1{
        margin: 0;
        padding: 0;
        font-size: 10cqmin;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        color: white;
        z-index: 1;
        font-weight: 300;
    }
    .landing{
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
        position: relative;
        background-size: cover;
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