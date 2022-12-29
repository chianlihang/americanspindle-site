<script>
    let premilling=false;
    const togglePremilling = () => {
        premilling=!premilling;
    }
    let finetrimming=false;
    const toggleFinetrimming = () => {
        finetrimming=!finetrimming;
    }
    let endtrimming=false;
    const toggleEndtrimming = () => {
        endtrimming=!endtrimming;
    }
    let hsk25r=false;
    const toggleHsk25r = () => {
        hsk25r=!hsk25r;
    }
</script>

<div id="menu" class="landing split">
    <div id="menuBox">
        <div id="menuGrid">
            <a id="one" on:mouseenter={togglePremilling} on:mouseleave={togglePremilling} href="/products/hfm/#contact">
                <img id="thumbnail" src="/img/hfm/premilling.png" alt="Pre-milling motors.">
                <h4 id="caption">Pre-milling</h4>
            </a>
    
            <a id="two" on:mouseenter={toggleFinetrimming} on:mouseleave={toggleFinetrimming} href="/products/hfm/#contact">
                <img id="thumbnail" src="/img/hfm/finetrimming.png" alt="Pre-milling motors.">
                <h4 id="caption">Fine-trimming</h4>
            </a>
    
            <a id="three" on:mouseenter={toggleEndtrimming} on:mouseleave={toggleEndtrimming} href="/products/hfm/#contact">
                <img id="thumbnail" src="/img/hfm/endtrimming.png" alt="Pre-milling motors.">
                <h4 id="caption">End-trimming</h4>
            </a>
    
            <a id="four" on:mouseenter={toggleHsk25r} on:mouseleave={toggleHsk25r} href="/products/hfm/#contact">
                <img id="thumbnail" src="/img/hfm/finetrimming_hsk25r.png" alt="Pre-milling motors.">
                <div id="caption">
                    <h4>HSK25R</h4>
                    <p style="color: var(--teknowhite);">Fine-trimming</p>
                </div>
            </a>
        </div>
    </div>

    <div id="descBox">
        <div id="hfmDesc">
            {#if premilling}
                <h1 class="centerText whiteText">Pre-milling</h1>
                <br>
                <p class="centerText whiteText">
                    Pre-milling units motor spindles work the edge of the panel in order to eliminate imperfections and moisture before the next gluing phase. High power, high precision, deep cuts, shaft by customer design, and direct tool mounting are some of the key features of our motors for this kind of application.            
                </p>
            {:else if finetrimming}
                <h1 class="centerText whiteText">Fine-trimming</h1>
                <br>
                <p class="centerText whiteText">
                    Motors of these types are used to complete panel finishing. Typical applications are trimming top and bottom, excess edging, chamfering, rounding corners. Their cylindrical shaft is manufactured according to customer specifications. With direct tool mounting, these motors are equipped like all Teknomotor HFMs with special bearings to withstand machining stresses.
                </p>
            {:else if endtrimming}
                <h1 class="centerText whiteText">End-trimming</h1>
                <br>
                <p class="centerText whiteText">
                    After application of the banding, it’s time to remove the excess edging at the head and tail of the panel. End-trimming spindles are designed and developed to operate blades. Built with special bearings to withstand machining stresses, these motors allow the tool to be mounted directly on the motor shaft.
                </p>
            {:else if hsk25r}
                <h1 class="centerText whiteText">HSK25R</h1>
                <h2 class="centerText whiteText">Fine-trimming</h2>
                <br>
                <p class="centerText whiteText">
                    Repeatability and precision without compromises. The HSK25R shaft design combines the advantages of a conical coupling with the precision of a double contact joint. Thanks to an extremely precise relation between the cone diameter and the position of the cone shoulder, the tool is mounted with uncompromised repeatability and precision.
                </p>
            {:else }
                <h1 class="centerText whiteText">Select your high frequency motor.</h1>
            {/if}
        </div>
    </div>
</div>

<style>
    /* menu */
    #menu{
        background-color: var(--teknograck);
    }

    #menuBox{
        height: 100%;
        /* background-color: red; */
        position: relative;
    }

    @media screen and (max-width:35.56251em){
        #menuBox{
            margin-top: 8%;
        }
    }

    #descBox{
        height: 100%;
        /* background-color: blue; */
        position: relative;
    }

    #menuGrid{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        display: grid;
        gap: 0.5em;
        /* grid-auto-columns: calc(40vh + 1em); */
        grid-template-areas:
            'one   two '
            'three four'
        ;
    }

    @media screen and (min-width:35.5625em){
        #menuGrid{
            gap: 1em;
        }
    }

    #one, #two, #three, #four{
        height: 20vh;
        width: 20vh;
        border: .25rem solid var(--teknowhite);
        position: relative;
        background-color: var(--teknograck);
    }

    #one{
        grid-area: one;
    }

    #two{
        grid-area: two;
    }

    #three{
        grid-area: three;
    }

    #four{
        grid-area: four;
    }

    #one:hover, #two:hover, #three:hover, #four:hover{
        background-color: var(--teknogrey);
    }

    @media screen and (min-width:35.5625em){
        #one, #two, #three, #four{
            height: 30vh;
            width: 30vh;
            border: .375rem solid var(--teknowhite);
            position: relative;
            background-color: var(--teknograck);
        }
    }

    @media screen and (min-width:64em){
        #one, #two, #three, #four{
            height: 40vh;
            width: 40vh;
            border: .5rem solid var(--teknowhite);
            position: relative;
            background-color: var(--teknograck);
        }
    }

    #thumbnail{
        height: 75%;
        position: absolute;
        right: 0;
    }

    #hfmDesc{
        width: 90%;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    #caption{
        width: 100%;
        color: var(--teknowhite);
        text-align: center;
        position: absolute;
        bottom: 2.5%;
        left: 50%;
        transform: translateX(-50%);
    }
</style>