<script lang="ts">
    let submitStatus: string;
    const submitForm = async(data) => {
        submitStatus = "submitting"
        const formData = new FormData(data.currentTarget);

        const res = await fetch(
            "contact.json",
            {
                method: "POST",
                body: formData,
            }
        );

        const {message}:any = await res.json;
        submitStatus = message;
    };
</script>

<div class="container">
    <div class="subContainer">
        {#if submitStatus === "submitting"}
            <h4 class="centerText">submitting...</h4>
        {:else if submitStatus === "failed"}
            <h4 class="centerText">form submission failed :&#40;</h4>
        {:else if submitStatus === "success"}
            <h4 class="centerText">successfully submitted :D</h4>
        {:else}
            <form on:submit|preventDefault={submitForm}>

                <div id="contactForm">
                    <div id="contactForm-grid">
                        <div id="name">
                            <h3 class="whiteText centerText">Name</h3>
                            <input type="text" name="name">
                        </div>
                        <div id="email">
                            <h3 class="whiteText centerText">Email</h3>
                            <input class="shorttext" type="email" name="email">
                        </div>
                        <div id="message">
                            <h3 class="whiteText centerText">Message</h3>
                            <textarea name="message"></textarea>
                        </div>
                        <div id="company">
                            <h3 class="whiteText centerText">Company</h3>
                            <input type="text" name="company">
                        </div>
                        <div id="phone">
                            <h3 class="whiteText centerText">Phone</h3>
                            <input class="shorttext" type="tel" name="phone">
                        </div>
                    </div>
        
                    <button id="submit" type="submit"><h4 id="submitText">Submit</h4></button>
                </div>
            </form>
        {/if}
    </div>
</div>    

<style>
    #contactForm{
        background-color: var(--teknograck);
        padding: 5vh 5vw 5vh 5vw;
    }

    #contactForm-grid{
        display: grid;
        gap: 2em;
        grid-auto-columns: 1fr;
        grid-template-areas:
            'one  two  three three'
            'four five three three'
        ;
    }

    @media screen and (max-width:35.56251em){
        #contactForm-grid{
            column-gap: 1em;
            row-gap: 0.5em;
            grid-template-areas:
                'one   two'
                'four  five'
                'three three'
            ;        
        }
    }

    #name{
        grid-area: one;
        line-height: 1.5;
    }

    #email{
        grid-area: two;
        line-height: 1.5;
    }

    #message{
        grid-area: three;
        line-height: 1.5;
    }

    #company{
        grid-area: four;
        line-height: 1.5;
    }

    #phone{
        grid-area: five;
        line-height: 1.5;
    }

    input{
        font-size: large;
        width: 100%;
        background-color: var(--teknowhite);
    }

    textarea{
        font-size: large;
        resize: none;
        outline: none;
        width: 100%;
        height: calc(10vh);
        background-color: var(--teknowhite);
    }

    @media screen and (min-width:35.5625em){
        textarea{
            height: calc(100% - 1.5em - 10px);
        }
    }

    #submit{
        margin-top: 1em;
        padding: 2px;
        width: 20vw;
        transform: skew(-23.2deg);
        border: 3px solid var(--teknored);
        text-align: center;
        background-color: var(--teknored);
        display: block;
        margin-left: auto;
        margin-right: auto;
        color: var(--teknowhite);
    }

    @media screen and (min-width:35.5625em){
        #submit{
            margin-top: 1.5em;
            width: 10vw;
            padding: 5px;
            border: 5px solid var(--teknored);
        }
    }

    @media screen and (min-width:64em){
        #submit{
            width: 10vw;
        }
    }

    #submit:hover {
        cursor: pointer;
        background-color: rgb(45,45,45);
        color: var(--teknored);
    }

    #submitText {
        transform: skew(23.2deg);
    }
</style>