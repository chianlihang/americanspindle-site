<script>
    import Button from "$lib/components/reusable/button.svelte";
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

<div id="landing" class="landing">
    <div id="cover"></div>
    <div id="landingText" class="centerText">
        <h1><span style="color: var(--teknored);">BBS:</span></h1>
        <br>
        <h2>Big Blade Series</h2>
        <div id="button"><Button text="Contact" link="#contact"/></div>
    </div>
    <img id="landingImg" src="/img/bbs/BBS_BG.jpg" alt="Our Big Blade Series spindles.">
</div>

<!-- ph1 -->
<section id="ph1Box" class="landing">
    <div id="splitBox" class="split">
        <img id="threepics" class="order1" src="/img/bbs/BBS_Ph1.png" alt="Machinist's spindle.">

        <div id="rightBox" class="order2">
            <h2 style="color: var(--teknowhite);">
                SPECIALLY DESIGNED TO EXCEED
            </h2>
            <br>
            <h3 style="color: var(--teknowhite);">
                New Electric Motor Spindle Big Blades Series are specially designed for cutting wood, aluminum, and plastics with blades of diameter exceeding 400mm diameter.
            </h3>    
        </div>
    </div>
</section>
<div use:viewport
	on:enterViewport={makeWhite}
	on:exitViewport={makeGrack}
></div>

<!-- ph2 -->
<section id="ph2Box" class="landing">
    <div id=splitBox class="split">
        <div id="leftBox" class="order1">
            <h2>
                HIGH PRECISION, REDUCED OSCILLATION
            </h2>
            <br>
            <h3>
                BBS spindles offer high cutting precision by the reduced axial oscillation of the blade holder flanges. By angular contact bearings, they can reach a rotation speed of 9000rpm. Ideal for processing wood, aluminum, and plastic materials.
            </h3>
        </div>

        <img id="threepics" class="order2" src="/img/bbs/BBS_Ph2.png" alt="Entering the CNC.">
    </div>
</section>

<Contact/>
<div use:viewport
	on:enterViewport={makeWhite}
	on:exitViewport={makeGrack}
></div>

<style>
    #landing{
        position: relative;
    }

    #landingImg{
        object-fit: cover;
        height: 100%;
        width: 100vw;
        display: block;
        margin: auto;
        z-index: 98;
    }

    @media screen and (min-width:35.5625em){
        #landingImg{
            height: 100vh;
            width: 100%;
        }
    }

    @media screen and (min-width:64em){
        #landingImg{
            height: 100vh;
            width: 100%;
        }
    }

    #cover{
        z-index: 97;
        background-image: linear-gradient(var(--teknowhite), rgb(75, 100, 120));
        height: 100vh;
        width: 100%;
        position: absolute;
        top: 0;
        opacity: 0.5;
    }

    #landingText{
        z-index: 98;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    #button{
        width: 100%;
        height: 15vh;
        /* background-color: blue; */
        position: relative;
    }

    #ph1Box{
        background-color: var(--teknograck);
        position: relative;
    }

    #ph2Box{
        background-color: var(--teknowhite);
        position: relative;
    }

    #splitBox{
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        padding: 5%;
    }

    #threepics{
        display: block;
        margin: auto;
        width: 85vw;
        border-radius: var(--r5);
        border: 1px solid var(--grack_gentle);
        background-color: var(--grack);
        padding-bottom: 5%;
    }

    @media screen and (min-width:35.5625em){
        #threepics{
            width: 35vw;
            padding-bottom: 0%;
        }
    }

    @media (min-width: 64em){
        #threepics{
            width: 35vw;
        }
    }

    #leftBox{
        display: block;
        margin-top: auto;
        margin-bottom: auto;
        margin-right: 5%;
    }

    #rightBox{
        text-align: left;
        display: block;
        margin-top: auto;
        margin-bottom: auto;
        margin-left: 5%;
    }

    @media (max-width: 35.56251em){
        #leftBox{
            text-align: center;
            order: 1;
        }

        #rightBox{
            text-align: center;
            order: 2;
        }
    }
</style>