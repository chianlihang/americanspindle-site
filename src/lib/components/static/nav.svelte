<script lang="ts">
    let hide: boolean = true;

    let toggleHide = () => {
        hide = !hide;
    }

    export let isGrack = false;

    // dont remember why this needs to be here but error if not 
    $: innerWidth = 0

    let bool = false;
    let sign = "+";
    let display3 = "none";

    let display = "none";
    let togglemenu = () => {
        if(bool == true){
            setTimeout(function(){display = "none"}, 100);
            display3 = "none";
            sign2 = "+";
            display2 = "none";
        }else{
            display = "block";
        }
        bool = !bool;
    }
    
    let sign2 = "+";
    let display2 = "none";
    let textChange2 = () => {
        if(sign2 == "+"){
            sign2 = "-";
            display2 = "block";
        }else{
            sign2 = "+";
            display2 = "none"
        }
    }
</script>

<svelte:window bind:innerWidth/>

{#if innerWidth>568}
    <div id="banner">
        <a href="/"><img id="logo" src="/img/logo.png" alt="American Spindle logo."></a>

        <div class="split">
            <p class="contactBanner" class:isGrack={isGrack}>+1 908-812-2100 &nbsp; &nbsp; &nbsp; contact@americanspindle.com</p>
        
            <div id="nav" class="split">
                <div class="navBox"><a href="/"><h4 class:isGrack={isGrack}>Home</h4></a></div>

                <div id="products" on:mouseenter={toggleHide} on:mouseleave={toggleHide}>
                    <a class="navBox" href="/products"><h4 class:isGrack={isGrack}>Products</h4></a>
                    <div id="dropdown" class:hide={hide}>
                        <a class="navBox" href="/products/hfm"><h5 id="dropdownText">HFM</h5></a>
                        <a class="navBox" href="/products/mtce"><h5 id="dropdownText">MTCE</h5></a>
                        <a class="navBox" href="/products/atc"><h5 id="dropdownText">ATC</h5></a>
                        <a class="navBox" href="/products/bbs"><h5 id="dropdownText">BBS</h5></a>
                        <a class="navBox" href="/products/custom"><h5 id="dropdownText">Custom</h5></a>
                        <a class="navBox" href="/products/k"><h5 id="dropdownText">K Products</h5></a>
                        <a class="navBox" href="/products/accessories"><h5 id="dropdownText">Accessories</h5></a>
                    </div>
                </div>

                <div class="navBox"><a href="/about"><h4 class:isGrack={isGrack}>About</h4></a></div>

                <div class="navBox"><a href="/#contact"><h4 class:isGrack={isGrack}>Contact</h4></a></div>
            </div>
        </div>
    </div>
{:else}
    <!-- Mobile Nav -->
    <div id="banner">
        <a href="/"><img id="logo" src="/img/logo.png" alt="American Spindle logo."></a>

        <div id="menu" class:open={bool} on:click={togglemenu}>
            {#if bool}
                <div id="x1" class="x"></div>
                <div id="x2" class="x"></div>
            {:else}
                <div class:menuIsGrack={isGrack} id="ham1" class="hamburger"></div>
                <div class:menuIsGrack={isGrack} id="ham2" class="hamburger"></div>
                <div class:menuIsGrack={isGrack} id="ham3" class="hamburger"></div>
            {/if}
        </div>

        <nav class="mobileNav" style="display: {display}" class:slide={bool} class:slideleft={!bool}>
            <ul class="navLi">
                <li><a href="/"><h1 id="navh1" class="whiteText">Home</h1></a></li>
                <li>
                    <h1 id="navh1" class="whiteText"><a href="/products"><span>Products</span></a><span class="sign whiteText" on:click={textChange2}>&nbsp;&nbsp;{sign2}</span></h1>
                    <ul class="subMenu" style="display: {display2};">
                        <li><a href="/products/hfm" on:click={togglemenu}><h1 id="subText" class="whiteText">&nbsp; HFM</h1></a></li>
                        <li><a href="/products/mtce" on:click={togglemenu}><h1 id="subText" class="whiteText">&nbsp; MTCE</h1></a></li>
                        <li><a href="/products/qtce" on:click={togglemenu}><h1 id="subText" class="whiteText">&nbsp; QTCE</h1></a></li>
                        <li><a href="/products/atc" on:click={togglemenu}><h1 id="subText" class="whiteText">&nbsp; ATC</h1></a></li>
                        <li><a href="/products/bbs" on:click={togglemenu}><h1 id="subText" class="whiteText">&nbsp; BBS</h1></a></li>
                        <li><a href="/products/custom" on:click={togglemenu}><h1 id="subText" class="whiteText">&nbsp; Custom</h1></a></li>
                        <li><a href="/products/k" on:click={togglemenu}><h1 id="subText" class="whiteText">&nbsp; K Products</h1></a></li>
                        <li><a href="/products/accessories" on:click={togglemenu}><h1 id="subText" class="whiteText">&nbsp; Accessories</h1></a></li>
                    </ul>
                </li>
                <li><a href="/about"><h1 id="navh1" class="whiteText">About</h1></a></li>
                <li><a href="/#contact"><h1 id="navh1" class="whiteText">Contact</h1></a></li>
            </ul>
        </nav>
    </div>

    <!-- <div id="backdrop" on:click={togglemenu}></div> -->
{/if}

<style>
    .mobileNav{
        position: fixed;
        background-color: rgba(42.5,42.5,42.5,0.5);
        width: 100%;
        opacity:1;
        height:100%;
        backdrop-filter: blur(3px);
        margin-top: -10px;
    }

    /* #backdrop{
        height:120vh;
        width:100vw;
        background-color:var(--teknored);
        opacity:0.5;
        position: fixed;
        top: 0;
        left: 0;
    } */

    /* hamburger */
    #menu{
        /* clickbox matching logo */
        height: calc(8vh - 15px);
        width: 8vh;
        position: relative;
        /* background-color: var(--teknowhite); */
        float: right;
        margin-right: 20px;
        margin-top: 10px;
    }

    .hamburger{
        z-index: 99;
        position: absolute;
        height: 1.2vh;
        width: 7.5vh;
        background-color: var(--teknowhite);
    }

    #ham1{
        top: 0;
    }

    #ham2{
        top: 50%;
        transform: translateY(-50%);
    }

    #ham3{
        bottom: 0;
    }

    /* x */
    .x{
        z-index: 99;
        position: absolute;
        height: 1.2vh;
        width: 7.5vh;
        background-color: var(--teknowhite);
        top: 50%;
        transform: translateY(-50%);
    }

    #x1{
        transform: rotate(45deg);
    }

    #x2{
        transform: rotate(-45deg);
    }

    .navLi{
        padding: 10%;
    }

    .navLi li{
        padding-top: 5%;
        text-decoration: none;
    }

    .navLi li a:hover{
        text-decoration: none;
        font-weight: bold;
    }

    #navh1{
        font-size: 12.5vw;
    }

    #subText{
        font-size: 10vw;
        overflow: hidden;
        white-space: nowrap;
    }

    .sign{
        font-size: 12.5vw;
    }

    @media screen and (min-width:35.5625em){
        p{
            font-size:3vw;
        }
        .sign{
            font-size:5vw;
        }
    }

    .menuIsGrack{
        background-color: var(--teknograck);
    }

    /* regular nav */
    #banner{
        position: fixed;
        width: 100%;
        padding: 10px 0px 10px 0px;
        z-index: 99;
    }

    #nav{
        color: var(--teknowhite);
    }

    #logo{
        height: 8vh;
        float: left;
        margin-left: 10px;
    }

    @media screen and (min-width:35.5625em){
        #logo{
            height:9vh;
        }
    }

    @media screen and (min-width:64em){
        #logo{
            height: 12.5vh;
        }
    }

    .contactBanner{
        font-size: 1.1vw;
        float: left;
        margin-left: 2.5%;
        margin-right: 10%;
        color: var(--teknowhite);
    }

    .navBox{
        text-align: center;
    }

    .navBox:hover{
        cursor: pointer;
        opacity: 0.5;
    }

    #dropdown{
        background-color: rgba(237,28,36,0.75);
        width: 100%;
        color: var(--teknowhite);
        padding-top: 5%;
        padding-bottom: 5%;
    }

    #dropdownText{
        color: var(--teknowhite);
        line-height: 2;
        overflow: hidden;
        white-space: nowrap;
    }

    .isGrack{
        color: var(--teknograck);
    }

    @keyframes slideRight {
        from {
            transform: translateX(-100%)
        } to {
            transform: translateX(0%)
        }
    }

    .slide{
        animation: .5s alternate slideRight;
    }

    .slideleft{
        animation: .5s alternate slideRight2;
    }
</style>