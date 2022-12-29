<script lang="ts">
    import Nav from '$lib/components/static/nav.svelte'
    import ProductGallery from "$lib/components/static/productGallery.svelte";
    import Trustedby from "$lib/components/static/trustedby.svelte";
    import Contact from "$lib/components/static/contact.svelte";

    const loadImg = (name) =>
		fetch(`/productlanding.json`)
			.then((res) => {
				if (!res.ok) throw new Error('Fetch error');
				return res;
			})
			.then((res) => res.json());

	$: landingPromise = '/productlanding.json' && loadImg('/productlanding.json');

    let i:number = 0;
    const increment = () => {
        if(i==5){
            i=0;
            setTimeout(increment, 3500);
        } else {
            i++;
            setTimeout(increment, 3500);
        }
    }

    increment();
</script>

<Nav />

<div id="aboutTech" class="landing">
        {#if landingPromise}
            {#await landingPromise then landingImg}
                <img id="landingImg" src="{landingImg[i].src}" alt="{landingImg[i].title}">
            {:catch err}
                <pre>{err}</pre>
            {/await}
        {/if}
        <div id="aboutTechDesc" class="sidePadding">
        <div id="aboutTechText">
            <h4 class="centerText">
                Used in applications from woodworking to aerospace manufacturing, Teknomotors manufactures premium spindles in Quero Vas, Italy which are distributed by American Spindle in North America.
            </h4>
            <br>
            <a href="/products/#browse"><h3 id="explore" class="centerText">Explore Our Products</h3></a>
        </div>
    </div>
</div>

<ProductGallery/>

<!-- <Trustedby/> -->

<Contact/>

<style>
    #landingImg{
        width: 100%;
        height: 100vh;
        object-fit: cover
    }

    #aboutTech{
        position: relative;
    }

    #aboutTechDesc{
        background-color: rgb(42.5,42.5,42.5, 0.5);
        position: absolute;
        bottom: 0;
        color: var(--teknowhite);
        padding: 2.5%;
    }

    #explore:hover{
        opacity: 0.5;
    }
</style>