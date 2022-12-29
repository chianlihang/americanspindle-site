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

<div id="landingBox1" class="landing">
    <div id="landingBox2">
        <h1 id="landingText" class="centerText">Custom Projects</h1>
        <br><br>
        <h2 id="landingText" class="centerText">Our technology, specially adapted to fit your needs.</h2>
        <br>
        <h3 id="landingText" class="centerText">Contact us to develop your solution.</h3>
        <br>
        <div id="landingContact"><Button text="Contact" link="#contact"/></div>
    </div>
    <img id="landingImg" src="/img/landing.jpg" alt="Man holding spindle.">
</div>

<div id="productDiv" class="productDiv landing">
    <a href="#contact">    
        <div id="customCard" class="split">
            <img id="img" src="/img/custom/1.jpg" alt="HF motor with extra long shaft.">
            <div id="textBox">
                <h2 id="text">HF motor with extra long shaft for PVC application.</h2>
            </div>
        </div>
    </a>
</div>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>

<div id="productDiv" class="productDiv landing">
    <a href="#contact">
        <div id="customCard" class="split">
            <div id="textBox">
                <h2 id="text">Double shaft HF motor for robotic application.</h2>
            </div>
            <img id="img" src="/img/custom/2.jpg" alt="Double shaft HF motor for robotic application.">
        </div>
    </a>
</div>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>


<div id="productDiv" class="productDiv landing">
    <a href="#contact">
        <div id="customCard" class="split">
            <img id="img" src="/img/custom/3.jpg" alt="MTCE with electric plug in rear.">
            <div id="textBox">
                <h2 id="text">Manual tool change electro spindle with electric plug in rear position.</h2>
            </div>
        </div>
    </a>
</div>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>


<div id="productDiv" class="productDiv landing">
    <a href="#contact">
        <div id="customCard" class="split">
            <div id="textBox">
                <h2 id="text">Manual tool change electro spindle with a long nose and long shaft.</h2>
            </div>
            <img id="img" src="/img/custom/4.jpg" alt="MTCE with long nose and shaft.">
        </div>
    </a>
</div>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>


<Contact/>

<style>
    #landingBox1{
        position: relative;
        background-color: var(--teknograck);
    }

    #landingBox2{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        z-index: 97;
    }

    #landingImg{
		position: absolute;
        width: 100%;
        height: 100vh;
        object-fit: cover;
		z-index: 1;
    }

    #landingText{
        color: var(--teknowhite);
    }

    #landingContact{
        height: 15vh;
        width: 100%;
        position: relative;
    }

    /* Product Divs starting */
    .productDiv{
        position: relative;
    }

    #customCard{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 75%;
        height: 75%;
        box-shadow: 5px 10px 18px var(--teknogrey);
        /* background-color: var(--teknored); */
    }

    #img{
        object-fit: cover;
        height: 100%;
        /* width: 100%; */
        /* height: 100%; */
    }

    @media screen and (min-width:35.5625em){
        #img{
            width: 45vw;
            height: 100%;
        }
    }

    @media screen and (min-width:64em){
        #img{
            width: 40vw;
        }
    } 

    #textBox{
        position: relative;
        /* height: 40vh;
        width: 40vw; */
        height: 100%;
        background-color: var(--teknored);
    }

    @media (max-width: 35.56251em){
        #img{
            order: 1;
        }

        #textBox{
            order: 2;
        }
    }

    #text{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: var(--teknowhite);
        width: 80%;
    }
</style>