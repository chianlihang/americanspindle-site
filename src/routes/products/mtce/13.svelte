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
    id="mtce/13"
    name="3140-D-DBS-P-ER20-RH"
    desc="The electrospindle 3140 SERIES are designed to generate high power with a limited overall dimensions. These characteristics, combined with the high rotational speed, making them ideal for use on machines for working wood, aluminum and PVC. SERIES 3140: for a 12,000 rpm to 24,000 rpm when the load is radial and axial." 
    toolholder="ER20"
    power="0.75 kW"
    dutycycle="S1"
    torque="0.60 Nm"
    normalspeed="12000 RPM"
    maxspeed="24000 RPM"
    voltage="220 V, 380 V"
    weight="4.42 kg"
    ordercode="COM31400313"
/>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>

<Contact/>