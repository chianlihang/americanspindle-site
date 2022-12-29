<script>
    import Product from "$lib/components/reusable/product.svelte";

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
<Product 
    id="atc/5"
    name="ATC41-C-2DB-ISO20-SN-HY-LC"
    desc="The electrospindles series ATC41 have been designed to develop high power with limited overall dimensions and low weight, only 5.9kg. This type of electrospindle is suitable to be installed on automatic machines, robotic application, cnc routers and desktop routers for machining wood, aluminum, plastics and composite materials. Thanks to the stiffness of the mechanical components, the speed of tool changing and the goodness of electrical components of this electrospindle, Teknomotor wanted to offer a best in class product for the most demanding customers. This version is equipped with ISO20." 
    toolholder="ISO20"
    power="2.20 kW"
    dutycycle="S1"
    torque="0.88 Nm"
    normalspeed="24000 RPM"
    maxspeed="30000 RPM"
    voltage="220 V"
    weight="6.63 kg"
    ordercode="COMTC410007"
/>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>

<Contact/>