<script>

</script>

<div id="browse" class="landing">
	<h1 id="title" class="centerText whiteText">Browse Our Products</h1>

	<div id="productGrid">
		<a class="productBox" href="/products/hfm">
			<div id="productLabel" class="">
				<h2 id="acr">HFM</h2>
				<br>
				<h4>High <br> Frequency <br> Motors</h4>
			</div>
			<img id="teknoCircle" src="/img/teknoCircle.png" alt="Circle graphic.">
			<img id="product" src="/img/productThumbnails/hfmThumbnail.png" alt="High Frequency Motor.">
		</a>
		<a class="productBox" href="/products/mtce">
			<div id="productLabel" class="">
				<h2 id="acr">MTCE</h2>
				<br>
				<h4>Manual Tool<br>Change<br>Electrospindle</h4>
			</div>
			<img id="teknoCircle" src="/img/teknoCircle.png" alt="Circle graphic.">
			<img id="product" src="/img/productThumbnails/mtceThumbnail.png" alt="Manual Tool Change Spindle.">
		</a>
		<a class="productBox" href="/products/qtce">
			<div id="productLabel" class="">
				<h2 id="acr">QTCE</h2>
				<br>
				<h4>Quick Tool<br>Change<br>Electrospindle</h4>
			</div>
			<img id="teknoCircle" src="/img/teknoCircle.png" alt="Circle graphic.">
			<img id="product" src="/img/productThumbnails/qtceThumbnail.png" alt="Quick Tool Change Spindle.">
		</a>
		<a class="productBox" href="/products/atc">
			<div id="productLabel" class="">
				<h2 id="acr">ATC</h2>
				<br>
				<h4>Automatic<br>Tool Change<br>Electrospindle</h4>
			</div>
			<img id="teknoCircle" src="/img/teknoCircle.png" alt="Circle graphic.">
			<img id="product" src="/img/productThumbnails/atcThumbnail.png" alt="Automatic Tool Change Spindle.">
		</a>
		<a class="productBox" href="/products/bbs">
			<div id="productLabel" class="">
				<h2 id="acr">BBS</h2>
				<br>
				<h4>Big Blade<br>Series</h4>
			</div>
			<img id="teknoCircle" src="/img/teknoCircle.png" alt="Circle graphic.">
			<img id="product" src="/img/productThumbnails/bbsThumbnail.png" alt="Big Blade Series Spindles.">
		</a>
		<a class="productBox" href="/products/custom">
			<div id="productLabel" class="">
				<h2 id="acr">Custom <br>Made <br>Solutions</h2>
			</div>
			<img id="teknoCircle" src="/img/teknoCircle.png" alt="Circle graphic.">
			<img id="product" src="/img/productThumbnails/customThumbnail.png" alt="Custom Made Solutions.">
		</a>
		<a class="kBox" href="/products/k">
			<img id="kThumbnail" src="/img/productThumbnails/kThumbnail.png" alt="Circle graphic.">
		</a>
		<a class="productBox" href="/products/accessories">
			<div id="productLabel" class="">
				<h2 id="acr">Acces- <br>sories</h2>
			</div>
			<img id="teknoCircle" src="/img/teknoCircle.png" alt="Circle graphic.">
			<img id="product" src="/img/productThumbnails/accessoriesThumbnail.png" alt="Accessories.">
		</a>
	</div>
</div>

<style>
    #browse{
		padding-left: 2.5%;
		padding-right: 2.5%;
		background-color: var(--teknogrey);
	}

	#title{
        padding-top: 2.5%;
        padding-bottom: 3.25%;
	}

	#productGrid{
		display: grid;
        gap: 1em;
        grid-auto-columns: 1fr;
        grid-template-areas:
            'one  two three four'
            'five six seven eight'
        ;
	}

	.productBox{
		background-color: var(--teknogrey);
		height: 30vh;
		border: 7.5px solid var(--teknowhite);
		position: relative;
		color: var(--teknowhite);
	}

	@media screen and (max-width:35.56251em){
        #productGrid{
			gap: 0.75em;
			grid-template-areas:
            'one   two'
            'three four'
			'five  six'
			'seven eight'
        ;     
        }

		.productBox{
			height: 17.5vh;
			border: 5px solid var(--teknowhite);
		}
    }

	#product{
		z-index: 1;
		position: absolute;
		right: 0;
		top: 50%;
		transform: translateY(-50%);
		z-index: 98;
		height: 90%;
	}
	
	#product:hover{
		height: 95%;
	}

	#teknoCircle{
		z-index: 1;
		position: absolute;
		top: 0;
		right: 0;
		height: 100%;
		max-width: 40%;
	}

	#acr{
		color: var(--teknowhite);
	}

	#productLabel{
		z-index: 97;
		float: left;
		margin-left: 10%;
		position: absolute;
		top: 50%;
		-ms-transform: translateY(-50%);
		transform: translateY(-50%);
	}

	#kThumbnail{
		width: 40%;
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
	}

	.kBox{
		background-color: rgb(45,45,45);
		border: 7.5px solid var(--teknowhite);
		position: relative;
	}

	@media screen and (max-width:35.56251em){
		.kBox{
			height: 17.5vh;
			border: 5px solid var(--teknowhite);
		}
    }
</style>