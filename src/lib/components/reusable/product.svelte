<script lang="ts">
    export let id:string;
    export let name:string;
    export let desc: string;

    export let toolholder:string;
    export let power: string;
    export let dutycycle:string;
    export let torque:string;
    export let normalspeed:string;
    export let maxspeed: string;
    export let voltage:string;
    export let weight:string;
    export let ordercode:string;
</script>

<div id="landing" class="landing">
    <img id="backgroundImg" src="/img/product_bg1.jpg" alt="">
    <div class="split">
        <div id="imgBox">
            <img id="img" src="/img/{id}.jpg" alt="{name}">
        </div>
        <div id="textBox">
            <div id="text">
                <h2 id="name">{name}</h2>
                <br>
                <p id="desc">{desc}</p>
            </div>
        </div>
    </div>
</div>

<div id="tech" class="landing">
    <div class="split">
        <div id="diagramBox" class="rightBox">
            <img id="diagram" src="/img/{id}_design.jpg" alt="{name} Diagram">
        </div>
        <div id="tableBox" class=" leftBox">
            <div id="table">
                <h2 class="centerText">
                    Technical Characteristics
                </h2>
    
                <br>
    
                <table>
                    <tr>
                        <td><h5>Tool Holder</h5></td>
                        <td><p>{toolholder}</p></td>
                    </tr>
                    <tr>
                        <td><h5>Power</h5></td>
                        <td><p>{power}</p></td>
                    </tr>
                    <tr>
                        <td><h5>Duty Cycle</h5></td>
                        <td><p>{dutycycle}</p></td>
                    </tr>
                    <tr>
                        <td><h5>Torque</h5></td>
                        <td><p>{torque}</p></td>
                    </tr>
                    <tr>
                        <td><h5>Normal Speed</h5></td>
                        <td><p>{normalspeed}</p></td>
                    </tr>
                    <tr>
                        <td><h5>Max Speed</h5></td>
                        <td><p>{maxspeed}</p></td>
                    </tr>
                    <tr>
                        <td><h5>Voltage</h5></td>
                        <td><p>{voltage}</p></td>
                    </tr>
                    <tr>
                        <td><h5>Weight</h5></td>
                        <td><p>{weight}</p></td>
                    </tr>
                    <tr>
                        <td><h5>Order Code</h5></td>
                        <td><p>{ordercode}</p></td>
                    </tr>
                </table>
            </div>
        </div>
    </div>
</div>

<style>
    #landing{
        position: relative;
    }

    #backgroundImg{
        position: absolute;
        width: 100%;
        height: 100vh;
        object-fit: cover;
        z-index: 0;
        transform: scaleX(-1);
    }

    #imgBox{
        position: relative;
        height: 50vh;
    }

    @media screen and (min-width:35.5625em){
        #imgBox{
            height: 100vh;
            background-image: linear-gradient(to right, var(--teknograck), var(--teknograck), var(--teknograck), var(--teknograck), rgba(252, 251, 245, 0));
        }
    }

    #img{
        /* border: 0.5px solid var(--teknograck); */
        width: 80%;
        box-shadow: 10px 10px 10px var(--teknograck);
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
    }

    #textBox{
        position: relative;
        height: 50vh;
    }

    #text{
        padding: 10%;
        position: absolute;
        bottom: 0;
        background-color: rgba(252, 251, 245, 0.75);
    }

    @media screen and (min-width:35.5625em){
        #textBox{
            height: 100vh;
        }

        #text{
            padding: 5%;
            top: 50%;
            transform: translateY(-50%);
            background-color: rgba(252, 251, 245, 0.75);
        }
    }

    #name, #desc{
        /* color: var(--teknowhite); */
    }

    /* tech */
    #tech{
        background-color: var(--teknowhite);
    }

    @media (max-width: 35.56251em){
        .leftBox{
            text-align: center;
            order: 1;
        }

        .rightBox{
            text-align: center;
            order: 2;
        }
    }

    #diagramBox{
        height: 30vh;
        position: relative;
        /* background-color: red; */
    }

    #diagram{
        width: 65%;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
    }

    @media screen and (min-width:35.5625em){
        #diagramBox{
            height: 100vh;
        }

        #diagram{
            width: 80%;
            top: 50%;
            transform: translate(-50%, -50%);
        }
    }

    #tableBox{
        position: relative;
        height: 70vh;
    }

    #table{
        width: 80%;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    @media screen and (min-width:35.5625em){
        #tableBox{
            height: 100vh;
        }

        #table{
            width: 80%;
        }
    }

    table{
        width: 100%;
    }

    tr:nth-child(odd) {
        background-color: var(--teknowhite);
    }

    tr:nth-child(even) {
        background-color: rgb(175, 175, 175);
    }

    td{
        border: 1px solid #dddddd;
        text-align: left;
        padding: 8px;
    }
</style>