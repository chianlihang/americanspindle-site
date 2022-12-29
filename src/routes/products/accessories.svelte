<script>
    import Accessorycard from "$lib/components/reusable/accessorycard.svelte";
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

<div id="background">
    <h1 id="title" class="centerText"><span style="color: var(--teknored);">Accessories</span></h1>

    <div id="grid">
        <!-- tool holders -->
        <h2 id="holders" class="centerText">Tool Holders</h2>

        <a id="one" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/iso20.png"
                title="ISO20"
                description="According to DIN69871 and DIN6499. AT3 precision class. ISO1940 G2.5 @24000rpm dynamic balance"
            />
        </a>
    
        <a id="two" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/iso30.png"
                title="ISO30"
                description="According to DIN69871 and DIN6499. AT3 precision class. ISO1940 G2.5 @24000rpm dynamic balance"
            />
        </a>
    
        <a id="three" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/hsk32.jpg"
                title="ISO32"
                description="According to DIN69871 and DIN6499. AT3 precision class. ISO1940 G2.5 @24000rpm dynamic balance"
            />
        </a>
    
        <a id="four" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/hsk63.jpg"
                title="HSK63"
                description="According to DIN69871 and DIN6499. AT3 precision class. ISO1940 G2.5 @24000rpm dynamic balance"
            />
        </a>

        <!-- collets -->
        <h2 id="collets" class="centerText">Collets</h2>
        <a id="five" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/er11.jpg"
                title="ER11"
                description="ER11 collets designed to lock cylindrical shank tools."
            />
        </a>
    
        <a id="six" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/er16.jpg"
                title="ER16"
                description="ER16 collets designed to lock cylindrical shank tools."
            />
        </a>

        <a id="seven" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/er20.jpg"
                title="ER20"
                description="ER20 collets designed to lock cylindrical shank tools."
            />
        </a>
    
        <a id="eight" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/er25.jpg"
                title="ER25"
                description="ER25 collets designed to lock cylindrical shank tools."
            />
        </a>
    
        <a id="nine" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/er32.jpg"
                title="ER32"
                description="ER32 collets designed to lock cylindrical shank tools."
            />
        </a>

        <!-- nuts -->
        <h2 id="nuts" class="centerText">Nuts</h2>
        <a id="thirteen" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/gts11.jpg"
                title="GTS11"
                description=""
            />
        </a>
    
        <a id="fourteen" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/gts16.jpg"
                title="GTS16"
                description=""
            />
        </a>

        <a id="fifteen" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/gts20.jpg"
                title="GTS20"
                description=""
            />
        </a>
    
        <a id="sixteen" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/gts25.jpg"
                title="GTS25"
                description=""
            />
        </a>
    
        <a id="seventeen" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/gts32.jpg"
                title="GTS32"
                description=""
            />
        </a>

        <!-- wrenches -->
        <h2 id="wrenches" class="centerText">Wrenches</h2>
        <a id="twentyone" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/gts16_wrench.jpg"
                title="GTS16"
                description="GTS16 wrenches are designed to screw and unscrew GTS16 nuts."
            />
        </a>
    
        <a id="twentytwo" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/gts20_wrench.jpg"
                title="GTS20"
                description="GTS20 wrenches are designed to screw and unscrew GTS20 nuts"
            />
        </a>
    
        <a id="twentythree" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/gts25_wrench.jpg"
                title="GTS25"
                description="GTS25 wrenches are designed to screw and unscrew GTS25 nuts"
            />
        </a>
    
        <a id="twentyfour" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/gts32_wrench.jpg"
                title="GTS32"
                description="GTS32 wrenches are designed to screw and unscrew GTS32 nuts"
            />
        </a>

        <!-- tool holder setup stands and forks -->
        <h2 id="standfork" class="centerText">Tool Holder Setup Stands & Forks</h2>
        <a id="twentyfive" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/iso20_stand.jpg"
                title="ISO20 Tool Holder Setup Stand"
                description=""
            />
        </a>
    
        <a id="twentysix" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/iso30_stand.jpg"
                title="ISO30 Tool Holder Setup Stand"
                description=""
            />
        </a>
    
        <a id="twentyseven" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/hsk63_stand.jpg"
                title="HSK63 Tool Holder Setup Stand"
                description=""
            />
        </a>
    
        <a id="twentyeight" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/iso20_fork.jpg"
                title="ISO20 Fork"
                description="Fork for tool holder made of ABS, very lightweight, elastic, and resistant thermoplastic polymer."
            />
        </a>
    
        <a id="twentynine" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/iso30_fork.jpg"
                title="ISO30 Fork"
                description="Fork for tool holder made of ABS, very lightweight, elastic, and resistant thermoplastic polymer."
            />
        </a>

        <a id="thirty" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/hsk63f_fork.jpg"
                title="HSK63F Fork"
                description="Fork for tool holder made of ABS, very lightweight, elastic, and resistant thermoplastic polymer."
            />
        </a>

        <!-- cable sets for atc41 -->
        <h2 id="cables" class="centerText">Cable Sets For ATC41</h2>
        <a id="thirtythree" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/atc41_1.png"
                title="2m Single-Ended Cordset"
                description="M8x1-Female, Straight, 3-pin, A-coded, PUR black, 2 m, Drag chain compatible."
            />
        </a>
     
        <a id="thirtyfour" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/atc41_2.png"
                title="5m Single-Ended Cordset"
                description="M8x1-Female, Straight, 3-pin, A-coded, PUR black, 5 m, Drag chain compatible."
            />
        </a>
     
        <a id="thirtyfive" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/atc41_3.png"
                title="Junction Blocks"
                description="4x M8x1-Female, 3-pin, PUR black, 5.00 m, Drag chain compatible"
            />
        </a>
    
        <a id="thirtysix" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/atc41_4.png"
                title="Junction Blocks"
                description="6x M8x1-Female, 3-pin, PUR black, 5.00 m, Drag chain compatible."
            />
        </a>

        <!-- cable sets for accessories71 -->
        <h2 id="signal" class="centerText">Signal Cable</h2>
        <a id="thirtyseven" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/atc71_1.jpg"
                title="4147-C-DB-HSK32C-HY"
                description="3x(2×0.14) + 2×0.50. Shielded green cable with connector."
            />
        </a>
    
        <a id="thirtyeight" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/atc71_2.jpg"
                title="Power Cable"
                description="4G2.5+2x(2×1). Shielded orange cable with connector"
            />
        </a>

        <!-- inverters -->
        <h2 id="inverters" class="centerText">Inverters</h2>
        <a id="fourtyone" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/onephase.jpg"
                title="One Phase Inverter"
                description="Suitable for small applications up to 2.2 kW. Voltage supply up to 230V."
            />
        </a>
    
        <a id="fourtytwo" href="#contact">
            <Accessorycard
                thumbnail="/img/accessories/threephase.jpg"
                title="Three Phase Inverter"
                description="Suitable for every industrial application up to 15 kW. Voltage supply up to 400V."
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
        padding-top: 5%;
        padding-bottom: 2%;
    }

    #grid{
        padding: 2em;
        display: grid;        
        gap: 1em;
        grid-template-areas:
            'holders holders'
            'holders holders'
            'one two'
            'three four'
            'collets collets'
            'collets collets'
            'five six'
            'seven eight'
            'nine ten'
            'eleven twelve'
            'nuts nuts'
            'nuts nuts'
            'thirteen fourteen'
            'fifteen sixteen'
            'seventeen eighteen'
            'nineteen twenty'
            'wrenches wrenches'
            'wrenches wrenches'
            'twentyone twentytwo'
            'twentythree twentyfour'
            'standfork standfork'
            'standfork standfork'
            'twentyfive twentysix'
            'twentyseven twentyeight'
            'twentynine thirty'
            'thirtyone thirtytwo'
            'cables cables'
            'cables cables'
            'thirtythree thirtyfour'
            'thirtyfive thirtysix'
            'signal signal'
            'signal signal'
            'thirtyseven thirtyeight'
            'thirtynine fourty'
            'inverters inverters'
            'inverters inverters'
            'fourtyone fourtytwo'
            'fourtythree fourtyfour'
        ;
    }

    @media screen and (min-width:35.5625em){
        #grid{
            padding: 2em;
            display: grid;        
            gap: 2em;
            grid-template-areas:
                'holders holders holders holders'
                'one two three four'
                'collets collets collets collets'
                'five six seven eight'
                'nine ten eleven twelve'
                'nuts nuts nuts nuts'
                'thirteen fourteen fifteen sixteen'
                'seventeen eighteen nineteen twenty'
                'wrenches wrenches wrenches wrenches'
                'twentyone twentytwo twentythree twentyfour'
                'standfork standfork standfork standfork'
                'twentyfive twentysix twentyseven twentyeight'
                'twentynine thirty thirtyone thirtytwo'
                'cables cables cables cables'
                'thirtythree thirtyfour thirtyfive thirtysix'
                'signal signal signal signal'
                'thirtyseven thirtyeight thirtynine fourty'
                'inverters inverters inverters inverters'
                'fourtyone fourtytwo fourtythree fourtyfour'
            ;
        }
    }

    #holders{
        grid-area: holders;
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

    #collets{
        grid-area: collets;
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

    #nuts{
        grid-area: nuts;
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

    #wrenches{
        grid-area: wrenches;
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

    #standfork{
        grid-area: standfork;
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

    #cables{
        grid-area: cables;
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

    #signal{
        grid-area: signal;
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

    #inverters{
        grid-area: inverters;
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