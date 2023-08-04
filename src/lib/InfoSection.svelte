<script>
    import picture from '$lib/assets/uva_rotunda_dome.jpg' // placeholder for a second, will export as prop
    /**@type {boolean}*/
    export let mobile;
</script>

<div class="info-section" class:mobile style="background-image: url({picture});">
        <div class="row" class:mobile>
            <div class="text-content" class:mobile>
                <h1>Title</h1>  <!--  export as prop -->
                <p>Description</p> <!--  export as prop -->
            </div>
        </div>
</div>

<style>
    *{
        color: white;
        margin: 0;
        padding: 0;
    }
    .info-section{
        width: 100%;
        background-position: center;
        background-size: cover;
        display: flex;
        align-items: flex-end;
        height: 100%;
        box-sizing: border-box;
    }
    .row{
        display: flex;
        flex: 1;
        justify-content: end;
        margin-bottom: 7cqh;
    }
    .text-content{
        background-color: black;
        width: 40cqw;
        height: 40cqh;
        margin-right: -15cqw;
        text-align: center;
        padding-top: 5%;
        box-sizing: border-box;
    }
    .mobile{
        margin: 0;
        justify-content: center;
        align-items: center;
    }
</style>