<script>
    /**@type {boolean}*/
    export let mobile;
    /**@type {String}*/
    export let title;
    /**@type {String}*/
    export let text;
    export let picture;
</script>

<div class="info-section" class:mobile style="background-image: url({picture});">
        <div class="row" class:mobile>
            <div class="text-content" class:mobile>
                <h1>{title}</h1>
                <p>{text}</p> 
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
        height: 100vh;
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
        min-height: 40cqh;
        margin-right: -15cqw;
        text-align: center;
        padding-top: 5%;
        box-sizing: border-box;
        font-weight: 100;
    }
    h1{
        margin-bottom: 1cqh;
        font-size: 3.75cqmin;
    }
    p, h1{
        text-align: left;
        padding-left: 1cqw;
    }
    p{
        font-size: 2.75cqmin;
    }
    .mobile{
        margin: 0;
        justify-content: center;
        align-items: center;
    }
    .mobile *{
        text-align: center;
        padding-left: 0;
    }
    .text-content.mobile{
        width: 60cqw;
    }
</style>