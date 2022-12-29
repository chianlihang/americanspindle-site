<script lang="ts">
    export let profilePic: string;
    export let name: string;
    export let jobDesc: string;
    export let phone: string;
    export let email: string;
    export let intro: string = "";
</script>

<div id="container">
    <div id="split">
        <img
            id="profilePic"
            src={profilePic}
            alt="{name}'s profile pic."
        >

        <div id="text" class="centerText">
            <h3 id="name">{name}</h3>

            <div id="jobDescWrapper">
                <p id="jobDesc">{jobDesc}</p>
            </div>

            <p id="phoneEmail">{phone}</p>
            <p id="phoneEmail">{email}</p>

            <p id="intro">{intro}</p>
        </div>
    </div>
</div>

<style>
    #container{
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        color: var(--teknowhite);
        background-color: var(--teknored);
    }

    /* mobile styling */
    #split{
        display: flex;
        flex-direction: row;
    }

    img{
        /* height adapts to width. image size is determined by width. */
        min-width: 45vw;
        max-width: 45vw;
        height: 100%;
        object-fit: cover;
    }

    #text{
        padding: 5%;
        height: 100%;
        width: 47.5vw;
    }

    @media screen and (min-width:35.5625em){
        img{
            /* height adapts to width. image size is determined by width. */
            min-width: 25vh;
            max-width: 25vh;
            height: 100%;
            object-fit: cover;
        }
    }

    @media screen and (min-width:64em){
        #split{
            display: flex;
            flex-direction: row;
        }

        img{
            /* height adapts to width. image size is determined by width. */
            min-width: 40vh;
            max-width: 40vh;
            height: 100%;
            object-fit: cover;
        }

        #text{
            padding: 5%;
            height: 100%;
            width: 25vw;
        }
    }

    /* text styling */
    #name{
        font-weight: bold;
    }

    #jobDesc{
        line-height: 115%;
        color: var(--teknowhite);
        margin-bottom: 10%;
    }

    #phoneEmail{
        color: var(--teknowhite);
        font-size: 2.5vw;
    }

    #intro{
        color: var(--teknowhite);
        margin-top: 10%;
        font-size: 1.25vh;
    }

    @media screen and (min-width:35.5625em){
        #phoneEmail{
            font-size: 1.5vh;
        }

        #intro{
            font-size: 1.5vh;
        }
    }

    @media screen and (min-width:64em){
        #phoneEmail{
            font-size: 2vh;
        }

        #intro{
            font-size: 2.5vh;
        }
    }
</style>