<div class="landing quadrant">
    <div id="title">
        <h1 id="titleText"><span style="color:var(--teknored);">HFM:</span> High<br>Frequency<br>Motors</h1>
    </div>

    <div id="premilling-quad">
        <a href="/products/hfm/#menu"><img id="premilling-quad-pic" src="/img/hfm/premilling.png" alt="Pre-milling motors."></a>
        <h4 id="premilling-quad-label">Pre-milling</h4>
    </div>
    <div id="finetrimming-quad">  
        <h4 id="finetrimming-quad-label">Fine-trimming</h4> 
        <a href="/products/hfm/#menu"><img id="finetrimming-quad-pic" src="/img/hfm/finetrimming.png" alt="Pre-milling motors."></a> 
    </div>
    <div id="endtrimming-quad">
        <a href="/products/hfm/#menu"><img id="endtrimming-quad-pic" src="/img/hfm/endtrimming.png" alt="Pre-milling motors."></a>
        <h4 id="endtrimming-quad-label">End-trimming</h4>
    </div>
    <div id="hsk25r-quad">
        <div id="hsk25r-quad-label">
            <h4>HSK25R</h4>
            <p>Fine-trimming motors</p>
        </div>
        <a href="/products/hfm/#menu"><img id="hsk25r-quad-pic" src="/img/hfm/finetrimming_hsk25r.png" alt="Pre-milling motors."></a>
    </div>
</div>

<style>
    .quadrant{
        display: grid;
        grid-auto-columns: 1fr;
        grid-template-areas:
            'one   two'
            'three four'
        ;
        background-color: var(--teknograck);
        position: relative;
    }

    #title{
        position: absolute;
        text-align: center;
        top: 50%; right: 50%;
        transform: translate(50%,-50%);
        padding: 1.5rem;
    }

    #titleText{
        color: var(--teknowhite);
    }

    #premilling-quad-label, #endtrimming-quad-label{
        position: absolute;
        color: var(--teknowhite);
        top: 50%;
        transform: rotate(90deg) translateY(-50%);
        text-align: center;
    }

    #premilling-quad-label{
        left: 47.5%;
    }

    #endtrimming-quad-label{
        /* background-color: red; */
        width: 20vh;
        left: 34.5%;
    }

    #finetrimming-quad-label, #hsk25r-quad-label{
        position: absolute;
        color: var(--teknowhite);
        top: 50%;
        transform: rotate(-90deg) translateY(-50%);
        text-align: center;
    }

    #finetrimming-quad-label{
        right: 42.5%;
    }

    #hsk25r-quad-label{
        right: 40%;
    }

    @media screen and (min-width:35.5625em){
        #premilling-quad-label{
            left: 36%;
        }

        #endtrimming-quad-label{
            left: 32.5%;
        }

        #finetrimming-quad-label{
            right: 35%;
        }

        #hsk25r-quad-label{
            right: 35%;
        }
    }

    @media screen and (min-width:64em){
        #premilling-quad-label{
            left: 42.5%;
        }

        #endtrimming-quad-label{
            width: 30vh;
            left: 35%;
        }

        #finetrimming-quad-label{
            right: 42.5%;
        }

        #hsk25r-quad-label{
            right: 40%;
        }
    }

    #premilling-quad{
        grid-area: one;
        position: relative;
    }

    #premilling-quad-pic{
        position: absolute;
        top: 50%;
        transform: scaleX(-1) translateY(-50%);
        width: 75%;
    }

    @media screen and (min-width:35.5625em){
        #premilling-quad-pic{
            width: 50%;
        }
    }
    @media screen and (min-width:64em){
        #premilling-quad-pic{
            width: 50%;
        }
    }

    #finetrimming-quad{
        grid-area: two;
        position: relative;
    }

    #finetrimming-quad-pic{
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        width: 75%;
        right: 0;
    }

    @media screen and (min-width:35.5625em){
        #finetrimming-quad-pic{
            width: 50%;
        }
    }
    @media screen and (min-width:64em){
        #finetrimming-quad-pic{
            width: 50%;
        }
    }

    #endtrimming-quad{
        grid-area: three;
        position: relative;
    }

    #endtrimming-quad-pic{
        position: absolute;
        top: 50%;
        transform: scaleX(-1) translateY(-50%);
        width: 75%;
    }

    @media screen and (min-width:35.5625em){
        #endtrimming-quad-pic{
            width: 50%;
        }
    }
    @media screen and (min-width:64em){
        #endtrimming-quad-pic{
            width: 50%;
        }
    }

    #hsk25r-quad{
        grid-area: four;
        position: relative;
    }

    #hsk25r-quad-pic{
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        width: 75%;
        right: 0;
    }

    @media screen and (min-width:35.5625em){
        #hsk25r-quad-pic{
            width: 50%;
        }
    }
    @media screen and (min-width:64em){
        #hsk25r-quad-pic{
            width: 50%;
        }
    }

    #premilling-quad-pic:hover, #finetrimming-quad-pic:hover, #endtrimming-quad-pic:hover, #hsk25r-quad-pic:hover{
        width: 55%;
    }
</style>