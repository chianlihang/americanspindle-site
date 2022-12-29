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
    id="mtce/21"
    name="4147-B-DB-P-ER20-RH"
    desc="The electrospindle 4147 SERIES are designed to generate high power with a limited overall dimensions. These characteristics, combined with the high rotational speed, making them ideal for use on machines for working wood, aluminum and PVC. 4147 SERIES: for a 12,000 rpm to 24,000 rpm when the load is radial and axial." 
    toolholder="ER20"
    power="1.10 kW"
    dutycycle="S1"
    torque="0.88 Nm"
    normalspeed="12000 RPM"
    maxspeed="24000 RPM"
    voltage="220 V, 380 V"
    weight="6.51 kg"
    ordercode="COM41470492"
/>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>

<Contact/>