<script lang="ts">
    export let thumbnail:string
    export let title:string
    export let description:string
</script>

<div id="productCard">
    <img id="thumbnail" src={thumbnail} alt={title}/>
    <br>
    <h4 id="title">{title}</h4>
    <p id="desc">{description}</p>

</div>

<style>
    #productCard{
        width: 100%;
    }

    #thumbnail{
        background-color: white;
        object-fit: cover;
        width: 100%;
        box-shadow: 5px 5px 7.5px var(--teknogrey);
    }

    #title{
        text-align: center;
    }

    #desc{
        font-size: 2vw;
        text-align: center;
    }

    @media screen and (min-width:35.5625em){
        #desc{
            font-size: 1.25vw;
        }
    }

    @media screen and (min-width:64em){
        #desc{
            font-size: 1vw;
        }
    }
</style>