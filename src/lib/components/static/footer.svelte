<script>
  //updates + displays year for copyright in footer
  const getCurrentYear = () => {
    return new Date().getFullYear();
  }
</script>

<div id="footer">   
    <div class="split">
        <div>
            <a href="/"><img id="logo" src="/img/logo_box.png" alt="American Spindle logo."></a>
            <div class="centerText"><h3 class="whiteText">North America's <br> Teknomotor Distributor</h3></div>
        </div>
        <div id="footerInfo">
            <br>
            <br>
            <div class="centerText"><h4 class="whiteText">+1 908-812-2100</h4></div>
            <div class="centerText"><h4 class="whiteText">contact@americanspindle.com</h4></div>
            <div class="centerText"><h4 class="whiteText">39 Morris Street, Bridgewater, NJ 08807-2615</h4></div>
            <br>
            <div class="centerText"><p class="whiteText"><a href="/#contact">Contact</a> / <a href="/privacy">Privacy Policy</a> / <a href="/termsofuse">Terms of Use</a></p></div>
            <div class="centerText"><p class="whiteText">Designed by <a href="https://www.lanternfly.io">Lanternfly.io</a></p></div>
        </div>
    </div>

    <br>

    <!-- <div class="centerText"><p class="whiteText">Copyright &copy; {getCurrentYear()}, American Spindle</p></div> -->
    <br>
</div>

<style>
    #footer{
        background-color: var(--teknored);
    }

    #logo{
        width: 10vw;
        display: block;
        margin-left: auto;
        margin-right: auto;
    }

    @media screen and (max-width:35.56251em){
        #logo{
            width: 25vw;
        }
    }

    #footerInfo{
        display: block;
        margin: auto;
    }
</style>