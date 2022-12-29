<script>
    import Contactform from "./contactform.svelte";
</script>

<div id="contact" class="landing sidePadding">
	<h1 class="centerText whiteText">Contact</h1>
	<div id="line" class="line" style="background-color: var(--teknowhite);"></div>
	<div id="contactInfo" style="text-align: center;">
		<div id="one"><p class="whiteText">Phone: <br> +1 908-812-2100</p></div>
		<div id="two"><p class="whiteText">Email: <br> contact@americanspindle.com</p></div>
		<div id="three">
			<p class="whiteText">Mailing Address: <br> 39 Morris Street, <br> Bridgewater, NJ 08807-2615</p>
		</div>
		<div id="four"><p class="whiteText">Fax: <br> 908-231-1852</p></div>
	</div>
	<div id="line" class="line" style="background-color: var(--teknowhite);"></div>
	<Contactform/>
</div>

<style>
    #contact{
        padding-top: 2.5%;
		background-color: var(--teknogrey);
	}

	@media screen and (max-width:35.56251em){
        #contact{
            padding-top: 7.5%;        
        }
    }

	#line{
		margin-top: 5%;
		margin-bottom: 5%;
	}

	@media screen and (min-width:35.5625em){
		#line{
			margin-top: 2.5%;
			margin-bottom: 2.5%;
		}
	}

	.sidePadding{
		padding-left: 5%;
		padding-right: 5%;
	}

	#contactInfo{
		width: 100%;
        display: grid;        
        gap: 1em;
        grid-template-areas:
            'one two three four'
		;
	}

	@media screen and (max-width:35.56251em){
		#contactInfo{
			grid-template-areas:
				'one'		
				'two'
				'three'
				'four'
			;
			gap: 0.25em;
		}
	}

	#one{
        grid-area: one;
	}

	#two{
		grid-area: two;
	}

	#three{
		grid-area: three;
	}

	#four{
		grid-area: four;
	}
</style>