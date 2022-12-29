<script lang="ts">
    import Nav from '$lib/components/static/nav.svelte';
    import Teknomotor from "$lib/components/static/teknomotor.svelte";
    import Profile from "$lib/components/reusable/profile.svelte";

    // color changing
	import viewport from './useViewportAction';

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

<Nav isGrack={isGrack} />

<div id="processBox" class="landing">
    <img id="landingImg" src="/img/process.jpg" alt="Sales.">
    <div id="processTextBox">
        <h4>
            American Spindle focuses on B2B wholesale delivering stock or customized solutions for your company at scale. Getting in touch is easy - just contact sales at sales@americanspindle.com or visit our <a href="/#contact">contact page</a> to expect a smooth process to order and receive Teknomotor product.
        </h4>
    </div>
</div>

<Teknomotor/>
<div use:viewport
	on:enterViewport={makeGrack}
	on:exitViewport={makeWhite}
></div>

<div id="team" class="landing">
    <h1 id="teamText" class="centerText">Our Team</h1>
    <div id="profContainer-flex">
        <div id="profContainer" class="relative">
            <Profile
                profilePic='/img/adrian.jpg'
                name='Adrian Turcu'
                jobDesc='Sales'
                phone='+1 908-812-2100'
                email='adrian@americanspindle.com'
                intro="With 10+ years of running the company, Adrian is the one to talk to when it comes to anything Teknomotor related."
            />
        </div>
        <div id="profContainer" class="relative">
            <Profile
                profilePic='/img/simona.jpg'
                name='Simona Turcu'
                jobDesc='Accounting'
                phone='+1 908-812-2100'
                email='simona@americanspindle.com'
                intro="Simona's work keeps the company in order. Her diligence regarding company finances ensures that all is accounted for."
            />
        </div>
    </div>
</div>

<style>
    #profContainer-flex{
        width: 100%;
        display: flex;
        flex-direction: column;
        height: 80%;
        /* background-color: blue; */
    }

    @media screen and (min-width:35.5625em){
        #profContainer-flex{
            margin-top: 5vh;
        }
    }

    @media screen and (min-width:64em){
        #profContainer-flex{
            width: 100%;
            display: flex;
            flex-direction: row;
        }
    }

    #profContainer{
        flex: 1;
    }

    #processBox{
        position: relative;
    }

    #landingImg{
        width: 100%;
        height: 100vh;
        object-fit: cover
    }

    #processTextBox{
        background-color: rgb(42.5,42.5,42.5, 0.5);
        position: absolute;
        bottom: 0;
        color: var(--teknowhite);
        padding: 2.5%;
    }

    @media screen and (max-width:35.56251em){
        #processTextBox{
            padding: 5%;
        }
    }

    #team{
        background-color: var(--teknograck);
    }

    #teamText{
        color: var(--teknowhite);
        padding-top: 2.5%;
    }

    @media screen and (max-width:35.56251em){
        #teamText{
            padding-top: 7.5%;
            padding-bottom: 5%;        
        }
    }
</style>