<script lang="ts">
    export let thumbnail:string
    export let title:string
    export let cuttingMethod:string
    //{maxSpeed} is actually normal speed
    export let maxSpeed:string
    export let power:string
</script>

<div id="productCard">
    <img id="thumbnail" src={thumbnail} alt={title} />
    <br>
    <h4 id="title">{title}</h4>
    <p id="desc"><span style="font-weight: bold;">Cutting Method:</span> {cuttingMethod}</p>
    <!-- {maxSpeed} is actually normal speed -->
    <p id="desc"><span style="font-weight: bold;">Normal Speed:</span> {maxSpeed}</p>
    <p id="desc"><span style="font-weight: bold;">Power:</span> {power}</p>
</div>

<style>
    #productCard{
        width: 100%;
    }

    #thumbnail{
        width: 100%;
        box-shadow: 5px 5px 7.5px var(--teknogrey);
    }

    #title{
        text-align: center;
    }

    #desc{
        font-size: 1vw;
        text-align: center;
    }
</style>