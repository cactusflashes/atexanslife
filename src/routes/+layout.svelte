<style>
    @import url(styles/style.css);
    @import url('https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,500;0,600;0,700;0,800;1,400;1,500;1,600;1,700;1,800&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap');
</style>
<script>
	import { fly, fade, slide, scale } from 'svelte/transition';
	import { afterNavigate, disableScrollHandling } from '$app/navigation';
	import Navbar from './navbar.svelte'; 
	export let data;
	//this fixes the snap to the top on page transition. 
	afterNavigate(() => {
    	disableScrollHandling();
    	setTimeout(() => {
        scrollTo({ top: 0, behavior: 'instant' });
    	}, 300);
	});
</script>
<Navbar /> 
{#key data.pathname}
<div in:fly={{y:30, duration: 400, delay: 400 }} out:fly={{y:-30, duration: 400 }}>
    <slot />
</div>
{/key}