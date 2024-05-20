<script>
	import Navbar from "./navbar.svelte";
	import Footer from "./footer.svelte"; 
</script>

<Navbar />
<slot />
<Footer /> 

<style>
	@import url(styles/style.css);
	@import url("https://fonts.googleapis.com/css2?family=Alice&display=swap");
	@import url("https://fonts.googleapis.com/css2?family=Alice&family=Inter:wght@100..900&display=swap");
</style>
