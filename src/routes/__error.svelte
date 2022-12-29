<script>
    import Nav from "$lib/components/static/nav.svelte";
    import Button from "$lib/components/reusable/button.svelte";
</script>

<svelte:head>
  <title>404</title>
  <meta name="description" content="404 Page Not Found">
</svelte:head>

<Nav/>
<div id="landing" class="landing">
    <div id="absolute">
        <h1 class="whiteText centerText">404 Page Not Found</h1>
        <br>
        <h2 class="whiteText centerText">It looks like you tried to get to a non-existent page. If you'd like to go to the home page, click below!</h2>
        <div id="buttonBox">
            <Button link="/" text="Home" />
        </div>
    </div>
</div>

<style>
    #landing{
        background-color: var(--teknograck);
        position: relative;
    }

    #absolute{
        width: 75%;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
    
    #buttonBox{
        height: 15vh;
        position: relative;
    }
</style>