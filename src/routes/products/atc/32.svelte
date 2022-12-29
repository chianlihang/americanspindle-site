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
    id="atc/32"
    name="ATC71-C-ISO30-SN-4P"
    desc="The electrospindles series ATC71 have been designed to develop high power with limited overall dimensions. This type of electrospindle is suitable to be installed on automatic machines for machining wood, aluminum and plastics. Thanks to the stiffness of the mechanical components, the speed of tool changing and the goodness of electrical components of this electrospindle, Teknomotor wanted to offer a best in class product for the most demanding customers. This version is equipped with ISO30." 
    toolholder="ISO30"
    power="12.00 kW"
    dutycycle="S6 60%"
    torque="9.55 Nm"
    normalspeed="12000 RPM"
    maxspeed="24000 RPM"
    voltage="380 V"
    weight="23.28 kg"
    ordercode="COMTC710024"
/>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>

<Contact/>