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
    id="mtce/44"
    name="4147-D-DB-P-ER25-PR-HY-RH"
    desc="The electrospindle 4147 SERIES are designed to generate high power with a limited overall dimensions. These characteristics, combined with the high rotational speed, making them ideal for use on machines for working wood, aluminum and PVC. 4147 SERIES: for a 12,000 rpm to 24,000 rpm when the load is radial and axial." 
    toolholder="ER25"
    power="1.80 kW"
    dutycycle="S1"
    torque="1.43 Nm"
    normalspeed="12000 RPM"
    maxspeed="24000 RPM"
    voltage="220 V, 380 V"
    weight="9.63 kg"
    ordercode="COM41470547"
/>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>

<Contact/>