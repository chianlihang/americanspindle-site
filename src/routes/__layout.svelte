<script lang="ts">
  import '../styles/reset.css'
  import '../styles/global.css'
  import '../styles/reusableclasses.css'
  import '../styles/variables.css'

  import Footer from '$lib/components/static/footer.svelte'
</script>

<svelte:head>
  <title>American Spindle</title>
  <meta name="description" content= "American Spindle is North America's Teknomotor distributor. Used in applications from woodworking to aerospace manufacturing, Teknomotor manufactures premium spindles for use by your company.">
</svelte:head>

<main>
	<slot />
</main>

<footer>
  <Footer/>
</footer>

<style>
</style>
