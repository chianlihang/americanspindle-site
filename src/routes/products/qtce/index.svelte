<script>
    import Productcard from "$lib/components/reusable/productcard.svelte";
    import Contact from "$lib/components/static/contact.svelte";

    // color changing
    import Nav from "$lib/components/static/nav.svelte";
	import viewport from '../../useViewportAction';

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

<div id="background">
    <h1 id="title" class="centerText"><span style="color: var(--teknored);">QTCE:</span> Quick Tool <br> Change Electrospindle</h1>

    <div id="grid">
        <a id="one" href="/products/qtce/1">
            <Productcard
                thumbnail="/img/qtce/1.jpg"
                title="4147-C-DB-HSK32C-HY"
                cuttingMethod="Dry"
                maxSpeed="12000rpm"
                power="1.5kW"
            />
        </a>
    
        <a id="two" href="/products/qtce/2">
            <Productcard
                thumbnail="/img/qtce/2.jpg"
                title="4147-C-DB-HSK32C-HY"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="2.2kW"
            />
        </a>
    
        <a id="three" href="/products/qtce/3">
            <Productcard
                thumbnail="/img/qtce/3.jpg"
                title="4147-C-DB-HSK32C-SV-HY"
                cuttingMethod="Dry"
                maxSpeed="18000rpm"
                power="2.2kW"
            />
        </a>
    
        <a id="four" href="/products/qtce/4">
            <Productcard
                thumbnail="/img/qtce/4.jpg"
                title="5160-D-2DBS-HSKC40-HY"
                cuttingMethod="Dry"
                maxSpeed="6000RPM"
                power="2.2kW"
            />
        </a>
    
        <a id="five" href="/products/qtce/5">
            <Productcard
                thumbnail="/img/qtce/5.jpg"
                title="5160-D-2DBS-HSKC40-PR-HY"
                cuttingMethod="Dry/Wet/Dusty"
                maxSpeed="18000rpm"
                power="6.0kW"
            />
        </a>
    </div>
</div>

<Contact/>
<div use:viewport
	on:enterViewport={makeWhite}
	on:exitViewport={makeGrack}
></div>

<style>
    #background{
        background-color: var(--teknowhite);
    }

    #title{
        padding: 25% 5% 2% 5%;
    }

    @media screen and (min-width:64em){
        #title{
            padding-top: 5%;
            padding-bottom: 2%;        
        }
    }

    #grid{
        padding: 2em;
        display: grid;        
        gap: 1em;
        grid-template-areas:
            'one two'
            'three four'
            'five six'
            'seven eight'
            'nine ten'
            'eleven twelve'
        ;
    }

    @media screen and (min-width:35.5625em){
        #grid{
        padding: 2em;
        display: grid;        
        gap: 2em;
        grid-template-areas:
            'one two three four'
            'five six seven eight'
            'nine ten eleven twelve'
        ;
        }
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

    #five{
        grid-area: five;
    }
</style>