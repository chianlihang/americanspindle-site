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
    id="mtce/42"
    name="5160-D-2DB-P-ER25-HY-RH"
    desc="The electrospindle 5160 SERIES have been designed to generate a high power with limited overall dimension. These features, joined to the high rotational speed, make these electrospindles the best solution for the machinery of wood, aluminum and PVC. 5160 SERIES: for rotational speed from 12.000 rpm to 24.000 rpm where a radial and/or an axial load are present." 
    toolholder="ER25"
    power="5.60 kW"
    dutycycle="S1"
    torque="2.97 Nm"
    normalspeed="18000 RPM"
    maxspeed="24000 RPM"
    voltage="220 V, 380 V"
    weight="14.86 kg"
    ordercode="COM51600228"
/>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>

<Contact/>