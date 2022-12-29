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
    <h1 id="title" class="centerText"><span style="color: var(--teknored);">MTCE:</span> Manual Tool <br> Change Electrospindle</h1>

    <div id="grid">
        <a id="one" href="/products/mtce/1">
            <Productcard
                thumbnail="/img/mtce/1.jpg"
                title="3140-A-DBS-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000rpm"
                power="0.22kW"
            />
        </a>
    
        <a id="two" href="/products/mtce/2">
            <Productcard
                thumbnail="/img/mtce/2.jpg"
                title="3140-A-DBS-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="0.33kW"
            />
        </a>
    
        <a id="three" href="/products/mtce/3">
            <Productcard
                thumbnail="/img/mtce/3.jpg"
                title="3140-A-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000rpm"
                power="0.22kW"
            />
        </a>
    
        <a id="four" href="/products/mtce/4">
            <Productcard
                thumbnail="/img/mtce/4.jpg"
                title="3140-A-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="0.33kW"
            />
        </a>
    
        <a id="five" href="/products/mtce/5">
            <Productcard
                thumbnail="/img/mtce/5.jpg"
                title="3140-B-DBS-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000rpm"
                power="0.37kW"
            />
        </a>
    
        <a id="six" href="/products/mtce/6">
            <Productcard
                thumbnail="/img/mtce/6.jpg"
                title="3140-B-DBS-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="0.55kW"
            />
        </a>
    
        <a id="seven" href="/products/mtce/7">
            <Productcard
                thumbnail="/img/mtce/7.jpg"
                title="3140-B-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000rpm"
                power="0.37kW"
            />
        </a>
    
        <a id="eight" href="/products/mtce/8">
            <Productcard
                thumbnail="/img/mtce/8.jpg"
                title="3140-B-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="0.55kW"
            />
        </a>
    
        <a id="nine" href="/products/mtce/9">
            <Productcard
                thumbnail="/img/mtce/9.jpg"
                title="3140-C-DBS-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000rpm"
                power="0.55kW"
            />
        </a>
    
        <a id="ten" href="/products/mtce/10">
            <Productcard
                thumbnail="/img/mtce/10.jpg"
                title="3140-C-DBS-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="0.73kW"
            />
        </a>
    
        <a id="eleven" href="/products/mtce/11">
            <Productcard
                thumbnail="/img/mtce/11.jpg"
                title="3140-C-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000rpm"
                power="0.55kW"
            />
        </a>
    
        <a id="twelve" href="/products/mtce/12">
            <Productcard
                thumbnail="/img/mtce/12.jpg"
                title="3140-C-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="0.73kW"
            />
        </a>
    
        <a id="thirteen" href="/products/mtce/13">
            <Productcard
                thumbnail="/img/mtce/13.jpg"
                title="3140-D-DBS-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="0.75kW"
            />
        </a>
    
        <a id="fourteen" href="/products/mtce/14">
            <Productcard
                thumbnail="/img/mtce/14.jpg"
                title="3140-D-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000kW"
                power="0.73kW"
            />
        </a>
    
        <a id="fifteen" href="/products/mtce/15">
            <Productcard
                thumbnail="/img/mtce/15.jpg"
                title="4147-A-DB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="1.1kW"
            />
        </a>
    
        <a id="sixteen" href="/products/mtce/16">
            <Productcard
                thumbnail="/img/mtce/16.jpg"
                title="4147-A-DB-P-ER25-HY-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="1.8kW"
            />
        </a>
    
        <a id="seventeen" href="/products/mtce/17">
            <Productcard
                thumbnail="/img/mtce/17.jpg"
                title="4147-A-DB-P-ER25-RH"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="0.75kW"
            />
        </a>
    
        <a id="eighteen" href="/products/mtce/18">
            <Productcard
                thumbnail="/img/mtce/18.jpg"
                title="4147-A-DB-P-ER25-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="1.1kW"
            />
        </a>
    
        <a id="nineteen" href="/products/mtce/19">
            <Productcard
                thumbnail="/img/mtce/19.jpg"
                title="4147-A-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="0.75kW"
            />
        </a>
    
        <a id="twenty" href="/products/mtce/20">
            <Productcard
                thumbnail="/img/mtce/20.jpg"
                title="4147-A-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="1.1kW"
            />
        </a>
    
        <a id="twentyone" href="/products/mtce/21">
            <Productcard
                thumbnail="/img/mtce/21.jpg"
                title="4147-B-DB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="1.1kW"
            />
        </a>
    
        <a id="twentytwo" href="/products/mtce/22">
            <Productcard
                thumbnail="/img/mtce/22.jpg"
                title="4147-B-DB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="1.6kW"
            />
        </a>
    
        <a id="twentythree" href="/products/mtce/23">
            <Productcard
                thumbnail="/img/mtce/23.jpg"
                title="4147-B-DB-P-ER25-HY-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="1.6kW"
            />
        </a>
    
        <a id="twentyfour" href="/products/mtce/24">
            <Productcard
                thumbnail="/img/mtce/24.jpg"
                title="4147-B-DB-P-ER25-PR-HY-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="18000RPM"
                power="1.6kW"
            />
        </a>

        <a id="twentyfive" href="/products/mtce/25">
            <Productcard
                thumbnail="/img/mtce/25.jpg"
                title="4147-B-DB-P-ER25-PR-RH"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="1.1kW"
            />
        </a>
    
        <a id="twentysix" href="/products/mtce/26">
            <Productcard
                thumbnail="/img/mtce/26.jpg"
                title="4147-B-DB-P-ER25-PR-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="1.6kW"
            />
        </a>
    
        <a id="twentyseven" href="/products/mtce/27">
            <Productcard
                thumbnail="/img/mtce/27.jpg"
                title="4147-B-DB-P-ER25-RH"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="1.1kW"
            />
        </a>

        <a id="twentyeight" href="/products/mtce/28">
            <Productcard
                thumbnail="/img/mtce/28.jpg"
                title="4147-B-DB-P-ER25-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="1.6kW"
            />
        </a>

        <a id="twentynine" href="/products/mtce/29">
            <Productcard
                thumbnail="/img/mtce/29.jpg"
                title="4147-B-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="1.1kW"
            />
        </a>

        <a id="thirty" href="/products/mtce/30">
            <Productcard
                thumbnail="/img/mtce/30.jpg"
                title="4147-B-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="1.6kW"
            />
        </a>

        <a id="thirtyone" href="/products/mtce/31">
            <Productcard
                thumbnail="/img/mtce/31.jpg"
                title="4147-C-DB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="2.2kW"
            />
        </a>

        <a id="thirtytwo" href="/products/mtce/32">
            <Productcard
                thumbnail="/img/mtce/32.jpg"
                title="4147-C-DB-P-ER25-HY-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="2.2kW"
            />
        </a>

        <a id="thirtythree" href="/products/mtce/33">
            <Productcard
                thumbnail="/img/mtce/33.jpg"
                title="4147-C-DB-P-ER25-RH"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="1.5kW"
            />
        </a>

        <a id="thirtyfour" href="/products/mtce/34">
            <Productcard
                thumbnail="/img/mtce/34.jpg"
                title="4147-C-DB-P-ER25-RH"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="2.2kW"
            />
        </a>

        <a id="thirtyfive" href="/products/mtce/35">
            <Productcard
                thumbnail="/img/mtce/35.jpg"
                title="4147-C-SB-P-ER20-RH"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="1.5kW"
            />
        </a>

        <a id="thirtysix" href="/products/mtce/36">
            <Productcard
                thumbnail="/img/mtce/36.jpg"
                title="4147-C-SB-P-ER20-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="18000RPM"
                power="2.2kW"
            />
        </a>

        <a id="thirtyseven" href="/products/mtce/37">
            <Productcard
                thumbnail="/img/mtce/37.jpg"
                title="5160-A-2DB-P-ER25-HY-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="18000RPM"
                power="3.3kW"
            />
        </a>

        <a id="thirtyeight" href="/products/mtce/38">
            <Productcard
                thumbnail="/img/mtce/38.jpg"
                title="5160-A-2DB-P-ER32-HY-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="18000RPM"
                power="3.3kW"
            />
        </a>

        <a id="thirtynine" href="/products/mtce/39">
            <Productcard
                thumbnail="/img/mtce/39.jpg"
                title="5160-A-DB-P-ER25-PR-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="12000RPM"
                power="2.2kW"
            />
        </a>

        <a id="fourty" href="/products/mtce/40">
            <Productcard
                thumbnail="/img/mtce/40.jpg"
                title="5160-A-DB-P-ER25-PR-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="18000RPM"
                power="3.3kW"
            />
        </a>

        <a id="fourtyone" href="/products/mtce/41">
            <Productcard
                thumbnail="/img/mtce/41.jpg"
                title="5160-A-DB-P-ER32-PR-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="18000RPM"
                power="3.3kW"
            />
        </a>

        <a id="fourtytwo" href="/products/mtce/42">
            <Productcard
                thumbnail="/img/mtce/42.jpg"
                title="5160-D-2DB-P-ER25-HY-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="18000RPM"
                power="5.6kW"
            />
        </a>

        <a id="fourtythree" href="/products/mtce/43">
            <Productcard
                thumbnail="/img/mtce/43.jpg"
                title="4147-B-DB-P-ER25-PR-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="18000RPM"
                power="1.6kW"
            />
        </a>

        <a id="fourtyfour" href="/products/mtce/44">
            <Productcard
                thumbnail="/img/mtce/44.jpg"
                title="4147-D-DB-P-ER25-PR-HY-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="12000RPM"
                power="1.8kW"
            />
        </a>

        <a id="fourtyfive" href="/products/mtce/45">
            <Productcard
                thumbnail="/img/mtce/45.jpg"
                title="4147-D-DB-P-ER25-PR-RH"
                cuttingMethod="Wet/Dusty"
                maxSpeed="12000RPM"
                power="1.8kW"
            />
        </a>

        <a id="fourtysix" href="/products/mtce/46">
            <Productcard
            thumbnail="/img/mtce/46.jpg"
            title="4147-D-DB-P-ER25-PR-RH"
            cuttingMethod="Wet/Dusty"
            maxSpeed="18000RPM"
            power="2.7kW"
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
            'thirteen fourteen'
            'fifteen sixteen'
            'seventeen eighteen'
            'nineteen twenty'
            'twentyone twentytwo'
            'twentythree twentyfour'
            'twentyfive twentysix'
            'twentyseven twentyeight'
            'twentynine thirty'
            'thirtyone thirtytwo'
            'thirtythree thirtyfour'
            'thirtyfive thirtysix'
            'thirtyseven thirtyeight'
            'thirtynine fourty'
            'fourtyone fourtytwo'
            'fourtythree fourtyfour'
            'fourtyfive fourtysix'
            'fourtyseven fourtyeight'
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
            'thirteen fourteen fifteen sixteen'
            'seventeen eighteen nineteen twenty'
            'twentyone twentytwo twentythree twentyfour'
            'twentyfive twentysix twentyseven twentyeight'
            'twentynine thirty thirtyone thirtytwo'
            'thirtythree thirtyfour thirtyfive thirtysix'
            'thirtyseven thirtyeight thirtynine fourty'
            'fourtyone fourtytwo fourtythree fourtyfour'
            'fourtyfive fourtysix fourtyseven fourtyeight'
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

    #six{
        grid-area: six;
    }

    #seven{
        grid-area: seven;
    }

    #eight{
        grid-area: eight;
    }

    #nine{
        grid-area: nine;
    }

    #ten{
        grid-area: ten;
    }

    #eleven{
        grid-area: eleven;
    }

    #twelve{
        grid-area: twelve;
    }

    #thirteen{
        grid-area: thirteen;
    }

    #fourteen{
        grid-area: fourteen;
    }

    #fifteen{
        grid-area: fifteen;
    }

    #sixteen{
        grid-area: sixteen;
    }

    #seventeen{
        grid-area: seventeen;
    }

    #eighteen{
        grid-area: eighteen;
    }

    #nineteen{
        grid-area: nineteen;
    }

    #twenty{
        grid-area: twenty;
    }

    #twentyone{
        grid-area: twentyone;
    }

    #twentytwo{
        grid-area: twentytwo;
    }

    #twentythree{
        grid-area: twentythree;
    }

    #twentyfour{
        grid-area: twentyfour;
    }

    #twentyfive{
        grid-area: twentyfive;
    }

    #twentysix{
        grid-area: twentysix;
    }

    #twentyseven{
        grid-area: twentyseven;
    }

    #twentyeight{
        grid-area: twentyeight;
    }
    
    #twentynine{
        grid-area: twentynine;
    }
    
    #thirty{
        grid-area: thirty;
    }
    
    #thirtyone{
        grid-area: thirtyone;
    }
    
    #thirtytwo{
        grid-area: thirtytwo;
    }
    
    #thirtythree{
        grid-area: thirtythree;
    }
    
    #thirtyfour{
        grid-area: thirtyfour;
    }

    #thirtyfive{
        grid-area: thirtyfive;
    }

    #thirtysix{
        grid-area: thirtysix;
    }
    
    #thirtyseven{
        grid-area: thirtyseven;
    }
    
    #thirtyeight{
        grid-area: thirtyeight;
    }

    #thirtynine{
        grid-area: thirtynine;
    }

    #fourty{
        grid-area: fourty;
    }

    #fourtyone{
        grid-area: fourtyone;
    }

    #fourtytwo{
        grid-area: fourtytwo;
    }

    #fourtythree{
        grid-area: fourtythree;
    }

    #fourtyfour{
        grid-area: fourtyfour;
    }

    #fourtyfive{
        grid-area: fourtyfive;
    }

    #fourtysix{
        grid-area: fourtysix;
    }
</style>