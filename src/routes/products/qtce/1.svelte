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
    id="qtce/1"
    name="4147-C-DB-HSK32C-HY"
    desc="The electrospindle 4147 SERIES are designed to generate high power with a limited overall dimensions. These characteristics, combined with the high rotational speed, making them ideal for use on machines for working wood, aluminum and PVC. 4147 SERIES: for a 12,000 rpm to 24,000 rpm when the load is radial and axial." 
    toolholder="HSK32C"
    power="1.50 kW"
    dutycycle="S1"
    torque="1.19 Nm"
    normalspeed="12000 RPM"
    maxspeed="24000 RPM"
    voltage="220 V, 380 V"
    weight="8.15 kg"
    ordercode="COM41470545"
/>
<div use:viewport
    on:enterViewport={makeGrack}
    on:exitViewport={makeWhite}
></div>

<Contact/>