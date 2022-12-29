<script>
    import Landing from "$lib/components/static/hfm/landing.svelte";
    import Menu from "$lib/components/static/hfm/menu.svelte";
    import Contact from "$lib/components/static/contact.svelte";

    // color changing
    import Nav from "$lib/components/static/nav.svelte";
	import viewport from '../useViewportAction';

    let isGrack = false;

    const makeGrack = () => {
        isGrack = true;
        console.log(isGrack);
    }

    const makeWhite = () => {
        isGrack = false;
        console.log(isGrack);
    }
</script>

<Nav isGrack={isGrack}/>

<Landing/>

<div id="intro" class="landing split">
    <img id="introPic" src="/img/hfm/hfm_intro.jpg" alt="HFM application">
    <div id="introText">
        <h4 class="centerText">GET INSPIRED BY NEW APPLICATIONS</h4>
        <br>
        <p class="centerText">
            The motors of the High Frequency Motors (HFM) families were born to serve the industry of manufacturers of industrial machines for edging wooden panels for the furniture industry. The main features are power, precision, direct mounting of the tool, and the construction of the shaft according to customer specifications. These features have led to the development of hundreds of solutions, expanding the application possibilities of HFM spindles. Contact us: It will be a pleasure to listen to you and accompany you in choosing the right motor spindle for you.
        </p>
    </div>
</div>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>

<Menu/>

<Contact/>

<style>
    #intro{
        background-color: var(--teknowhite);
    }

    #introPic{
        max-height: 40vh;
        object-fit: cover;
    }

    @media screen and (min-width:35.5625em){
        #introPic{
            max-height: 50vh;
        }
    }

    @media screen and (min-width:64em){
        #introPic{
            max-height: 100%;
            height: 100%;
        }
    }

    #introText{
        margin: 10%;
    }
</style>