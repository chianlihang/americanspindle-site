<script>
    import Nav from "$lib/components/static/nav.svelte";
    import Productcard from "$lib/components/reusable/productcard.svelte";
    import Contact from "$lib/components/static/contact.svelte";

	// color changing
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

<Nav isGrack={isGrack} />

<div id="background">
    <h1 id="title" class="centerText"><span style="color: var(--teknored);">ATC:</span> Automatic Tool <br> Change Electrospindle</h1>

    <div id="grid">
        <a id="one" href="/products/atc/1">
            <Productcard
                thumbnail="/img/atc/1.jpg"
                title="ATC41-A-DB-ISO20-SN"
                cuttingMethod="Dry"
                maxSpeed="18000rpm"
                power="1.1kW"
            />
        </a>
    
        <a id="two" href="/products/atc/2">
            <Productcard
                thumbnail="/img/atc/2.jpg"
                title="ATC41-A-DB-ISO20-SN S1/S2"
                cuttingMethod="Dry"
                maxSpeed="18000RPM"
                power="1.1kW"
            />
        </a>
    
        <a id="three" href="/products/atc/3">
            <Productcard
                thumbnail="/img/atc/3.jpg"
                title="ATC41-C-2DB-ISO20-SN-HY"
                cuttingMethod="Dry"
                maxSpeed="24000rpm"
                power="2.2kW"
            />
        </a>
    
        <a id="four" href="/products/atc/4">
            <Productcard
                thumbnail="/img/atc/4.jpg"
                title="ATC41-C-2DB-ISO20-SN-HY S1/S2"
                cuttingMethod="Dry"
                maxSpeed="24000RPM"
                power="2.2kW"
            />
        </a>
    
        <a id="five" href="/products/atc/5">
            <Productcard
                thumbnail="/img/atc/5.jpg"
                title="ATC41-C-2DB-ISO20-SN-HY-LC"
                cuttingMethod="Wet"
                maxSpeed="24000rpm"
                power="2.2kW"
            />
        </a>
    
        <a id="six" href="/products/atc/6">
            <Productcard
                thumbnail="/img/atc/6.jpg"
                title="ATC71-A-ISO30-LN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="3.8kW"
            />
        </a>
    
        <a id="seven" href="/products/atc/7">
            <Productcard
                thumbnail="/img/atc/7.jpg"
                title="ATC71-A-ISO30-LN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="3.8kW"
            />
        </a>
    
        <a id="eight" href="/products/atc/8">
            <Productcard
                thumbnail="/img/atc/8.jpg"
                title="ATC71-A-ISO30-LN-2P-AC"
                cuttingMethod="Wet"
                maxSpeed="12000RPM"
                power="3.8/4.6kW"
            />
        </a>
    
        <a id="nine" href="/products/atc/9">
            <Productcard
                thumbnail="/img/atc/9.jpg"
                title="ATC71-A-ISO30-SN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000rpm"
                power="3.8kW"
            />
        </a>
    
        <a id="ten" href="/products/atc/10">
            <Productcard
                thumbnail="/img/atc/10.jpg"
                title="ATC71-A-ISO30-SN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="3.8kW"
            />
        </a>
    
        <a id="eleven" href="/products/atc/11">
            <Productcard
                thumbnail="/img/atc/11.jpg"
                title="ATC71-A-ISO30-SN-2P-AC"
                cuttingMethod="Wet"
                maxSpeed="12000rpm"
                power="3.8kW"
            />
        </a>
    
        <a id="twelve" href="/products/atc/12">
            <Productcard
                thumbnail="/img/atc/12.jpg"
                title="ATC71-A-ISO30-SN-4P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="5.0kW"
            />
        </a>

        <a id="thirteen" href="/products/atc/13">
            <Productcard
                thumbnail="/img/atc/13.jpg"
                title="ATC71-B-HSK63F-LN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="5.5kW"
            />
        </a>
    
        <a id="fourteen" href="/products/atc/14">
            <Productcard
                thumbnail="/img/atc/14.jpg"
                title="ATC71-B-HSK63F-LN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000kW"
                power="5.5/6.6kW"
            />
        </a>
    
        <a id="fifteen" href="/products/atc/15">
            <Productcard
                thumbnail="/img/atc/15.jpg"
                title="ATC71-B-ISO30-LN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="5.5kW"
            />
        </a>
    
        <a id="sixteen" href="/products/atc/16">
            <Productcard
                thumbnail="/img/atc/16.jpg"
                title="ATC71-B-ISO30-LN-4P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="7.5/9.0kW"
            />
        </a>
    
        <a id="seventeen" href="/products/atc/17">
            <Productcard
                thumbnail="/img/atc/17.jpg"
                title="ATC71-B-ISO30-SN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="5.5kW"
            />
        </a>
    
        <a id="eighteen" href="/products/atc/18">
            <Productcard
                thumbnail="/img/atc/18.jpg"
                title="ATC71-B-ISO30-SN-4P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="7.5/9.0kW"
            />
        </a>
    
        <a id="nineteen" href="/products/atc/19">
            <Productcard
                thumbnail="/img/atc/19.jpg"
                title="ATC71-C-HSK63F-LN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="7.5kW"
            />
        </a>
    
        <a id="twenty" href="/products/atc/20">
            <Productcard
                thumbnail="/img/atc/20.jpg"
                title="ATC71-C-HSK63F-LN-2P-AC"
                cuttingMethod="Wet"
                maxSpeed="12000RPM"
                power="7.5/9.0kW"
            />
        </a>
    
        <a id="twentyone" href="/products/atc/21">
            <Productcard
                thumbnail="/img/atc/21.jpg"
                title="ATC71-C-HSK63F-LN-4P"
                cuttingMethod="Dry"
                maxSpeed="6000RPM"
                power="5.5kW"
            />
        </a>
    
        <a id="twentytwo" href="/products/atc/22">
            <Productcard
                thumbnail="/img/atc/22.jpg"
                title="ATC71-C-HSK63F-LN-4P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="10.0-12.0kW"
            />
        </a>
    
        <a id="twentythree" href="/products/atc/23">
            <Productcard
                thumbnail="/img/atc/23.jpg"
                title="ATC71-C-HSK63F-LN-4P-AC"
                cuttingMethod="Wet"
                maxSpeed="6000RPM"
                power="5.5kW"
            />
        </a>
    
        <a id="twentyfour" href="/products/atc/24">
            <Productcard
                thumbnail="/img/atc/24.jpg"
                title="ATC71-C-HSK63F-SN"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="7.5-9.0kW"
            />
        </a>
            
        <a id="twentyfive" href="/products/atc/25">
            <Productcard
                thumbnail="/img/atc/25.jpg"
                title="ATC71-C-HSK63F-SN-HSK F20-AC"
                cuttingMethod="Wet"
                maxSpeed="6000RPM"
                power="5.5kW"
            />
        </a>
            
        <a id="twentysix" href="/products/atc/26">
            <Productcard
                thumbnail="/img/atc/26.jpg"
                title="ATC71-C-ISO30-LN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="7.5kW"
            />
        </a>
            
        <a id="twentyseven" href="/products/atc/27">
            <Productcard
                thumbnail="/img/atc/27.jpg"
                title="ATC71-C-ISO30-LN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="7.5kW"
            />
        </a>
            
        <a id="twentyeight" href="/products/atc/28">
            <Productcard
                thumbnail="/img/atc/28.jpg"
                title="ATC71-C-ISO30-LN-4P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="10.0-12.0kW"
            />
        </a>
            
        <a id="twentynine" href="/products/atc/29">
            <Productcard
                thumbnail="/img/atc/29.jpg"
                title="ATC71-C-ISO30-LN-4P-AC"
                cuttingMethod="Wet"
                maxSpeed="12000RPM"
                power="10.0-12.0kW"
            />
        </a>
            
        <a id="thirty" href="/products/atc/30">
            <Productcard
                thumbnail="/img/atc/30.jpg"
                title="ATC71-C-ISO30-SN"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="7.5-9.0kW"
            />
        </a>
            
        <a id="thirtyone" href="/products/atc/31">
            <Productcard
                thumbnail="/img/atc/31.jpg"
                title="ATC71-C-ISO30-SN-2P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="7.5kW"
            />
        </a>
            
        <a id="thirtytwo" href="/products/atc/32">
            <Productcard
                thumbnail="/img/atc/32.jpg"
                title="ATC71-C-ISO30-SN-4P"
                cuttingMethod="Dry"
                maxSpeed="12000RPM"
                power="10.0-12.0kW"
            />
        </a>
            
        <a id="thirtythree" href="/products/atc/33">
            <Productcard
                thumbnail="/img/atc/33.jpg"
                title="ATC71-C-ISO30-SN-4P-AC"
                cuttingMethod="Wet"
                maxSpeed="12000RPM"
                power="10.0-12.0kW"
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
</style>