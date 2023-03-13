<script>
	import '../app.css';
	import 'aos/dist/aos.css';
	import AOS from 'aos';
	import { onMount } from 'svelte';
  
	onMount(() => {
		AOS.init();
	});

	export let data;
</script>

<slot />
