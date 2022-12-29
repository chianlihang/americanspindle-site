<script lang="ts">
	import Nav from '$lib/components/static/nav.svelte';
	import Button from '$lib/components/reusable/button.svelte'
	import ProductGallery from '$lib/components/static/productGallery.svelte';
	import Teknomotor from '$lib/components/static/teknomotor.svelte';
	import Trustedby from '$lib/components/static/trustedby.svelte';
	import Contact from '../lib/components/static/contact.svelte';

	const loadFeature = (name) =>
		fetch(`/feature.json`)
			.then((res) => {
				if (!res.ok) throw new Error('Fetch error');
				return res;
			})
			.then((res) => res.json());

	$: featurePromise = '/feature.json' && loadFeature('/feature.json');

	let random:number = Math.floor(Math.random()*6)

	// color changing
	import viewport from './useViewportAction';

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

<Nav isGrack={isGrack} />

<div id="home" class="landing">
	<img id="landingImg" src="/img/landing.jpg" alt="Background texture.">
	<div class="split">
		<div id="intro">
			<h1 id="as" class="introText">American <br> Spindle</h1>
			<!-- <br><br> -->
			<h2 class="introText">North America's <br> Teknomotor <br> Distributor</h2>
			<div class="twocol">
				<div id="buttonBox">
					<Button text="Contact" link="/#contact" />
				</div>
				<div id="buttonBox">
					<Button text="Products" link="/products" />
				</div>
			</div>
		</div>

		<div id="featureSection">
			{#if featurePromise}
				{#await featurePromise then feature}
				<a href="/products/{feature[random].link}">
						<img id="feature" src="{feature[random].src}" alt="{feature[random].title}">
						<h3 id="featureText" class="centerText whiteText">
							<br>
							<span style="font-weight: 600;">Featured Product</span>
							<br>
							{feature[random].title}
						</h3>
					</a>
				{:catch err}
					<pre>{err}</pre>
				{/await}
			{/if}
		</div>
	</div>
</div>

<ProductGallery/>

<Teknomotor/>

<div use:viewport
	on:enterViewport={makeGrack}
	on:exitViewport={makeWhite}
></div>

<!-- <Trustedby/> -->

<Contact/>
<style>
	#home{
		position: relative;
	}

	/* background image */
	#landingImg{
		position: absolute;
        width: 100%;
        height: 100vh;
        object-fit: cover;
		z-index: 1;
    }

	#intro{
		padding: 15vh 5% 0 5%;
		flex: 0.5;	
		z-index: 97;
	}

	.introText{
		color: var(--teknowhite);
		padding-left: 7.5%;
		margin-bottom: 5%;
	}

	#as{
		font-weight: 500;
	}

	#featureSection{
		position: relative;	
		z-index: 97;
	}

	#feature{
		width: 60%;
		display: block;
		margin-left: auto;
		margin-right: auto;
		margin-top: 5%;
	}

	#feature:hover{
		width: 65%;
		cursor: pointer;
	}

	#featureText{
		width: 100%;
		/* border: 2px solid red; */
	}

	@media screen and (min-height:700px){
		#intro{
			height: 77.7vh;
			padding: 15vh 5% 0 5%;
			/* width: 40vw;	 */
			flex: 0.5;	
			z-index: 97;
		}

		.introText{
			color: var(--teknowhite);
			padding-left: 7.5%;
			margin-bottom: 5%;
		}

		#as{
			font-weight: 500;
		}

		#featureSection{
			position: relative;	
			z-index: 97;
			/* border: 2px solid red; */
		}

		#feature{
			width: 85%;
			display: block;
			margin-left: auto;
			margin-right: auto;
			margin-top: 5%;
		}

		#feature:hover{
			width: 90%;
			cursor: pointer;
		}

		#featureText{
			width: 100%;
			/* border: 2px solid red; */
		}
	}

    @media screen and (min-width:35.5625em){
		#intro{
			height: 77.7vh;
			padding: 22.5vh 5% 0 5%;
			/* width: 40vw;	 */
			flex: 0.5;	
			z-index: 97;
		}

        #featureSection{
			position: relative;	
        }

		#feature{
			width: 85%;
			position: absolute;
			top: 35%;
			left: 50%;
			-ms-transform: translate(-50%, -50%);
			transform: translate(-50%, -50%);
		}

		#feature:hover{
			width: 90%;
			cursor: pointer;
		}

		#featureText{
			position: absolute;
			top: calc(20% + 27.5vw);
			left: 50%;
			-ms-transform: translateX(-50%);
			transform: translateX(-50%);
		}
    }

	/* to resolve text moves too far down after width >569px */
	@media screen and (min-width:35.5625em) and ( min-height: 600px){
		#feature{
			top: 30%;
		}

		#featureText{
			top: calc(20% + 30vw);
		}
	}

	@media screen and (min-width:35.5625em) and ( min-height: 850px){
		#feature{
			top: 27.5%;
		}

		#featureText{
			top: calc(20% + 32.5vw);
		}
	}

	@media screen and (min-width:35.5625em) and ( min-height: 1000px){
		#feature{
			top: 25%;
		}

		#featureText{
			top: calc(20% + 30vw);
		}
	}

	/* to resolve text moves too far down after width >1024px */
	@media screen and (min-width:64em){
		#feature{
			top: 30%;
		}

		#featureText{
			top: calc(20% + 22.5vw);
		}
	}

	@media screen and (min-width:64em) and ( min-height: 600px){
		#feature{
			top: 30%;
		}

		#featureText{
			top: calc(20% + 23.5vw);
		}
	}

	@media screen and (min-width:64em) and ( min-height: 850px){
		#feature{
			top: 27.5%;
		}

		#featureText{
			top: calc(20% + 25vw);
		}
	}

	@media screen and (min-width:64em) and ( min-height: 1000px){
		#feature{
			top: 25%;
		}

		#featureText{
			top: calc(20% + 25vw);
		}
	}

	.twocol{
		display: flex;
        flex-direction: row;
	}

	.twocol > * {
        flex-basis: 100%;
    }

	#buttonBox{
		width: 50%;
		position: relative;
		height: 5vh;
		/* border: 2px solid blue; */
	}

	@media screen and (min-width:35.5625em){
		#buttonBox{
			width: 100%;
		}
	}
</style>