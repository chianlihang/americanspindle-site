<script lang="ts">
    export let link:string = ""
    export let text:string = "Button"
</script>

<div id="button" class="redText">
    <a href="{link}" class="redText"><h4 id="text">{text}</h4></a>
</div>

<style>
    #text{
        transform: skew(23.2deg);
    }

    #button:hover {
        cursor: pointer;
        background-color: rgb(0,0,0,0);
        color: var(--teknored);
    }

    #button {
        padding: 2px;
        min-width: 20vw;
        border: 3px solid var(--teknored);
        text-align: center;
        background-color: var(--teknored);
        color: var(--teknowhite);
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%) skew(-23.2deg);
    }

    @media screen and (min-width:35.5625em){
        #button{
            min-width: 15vw;
            padding: 5px;
            border: 5px solid var(--teknored);
        }
    }

    @media screen and (min-width:64em){
        #button{
            min-width: 10vw;
        }
    }
</style>