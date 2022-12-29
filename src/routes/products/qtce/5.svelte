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
    id="qtce/5"
    name="5160-D-2DBS-HSKC40-PR-HY"
    desc="The electrospindle 5160 SERIES have been designed to generate a high power with limited overall dimension. These features, joined to the high rotational speed, make these electrospindles the best solution for the machinery of wood, aluminum and PVC. 5160 SERIES: for rotational speed from 12.000 rpm to 24.000 rpm where a radial and/or an axial load are present." 
    toolholder="HSKC40"
    power="6.00 kW"
    dutycycle="S1"
    torque="3.18 Nm"
    normalspeed="18000 RPM"
    maxspeed="24000 RPM"
    voltage="220 V, 380 V"
    weight="14.09 kg"
    ordercode="COM51600433"
/>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>

<Contact/>