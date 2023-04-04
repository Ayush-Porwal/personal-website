<script>
	import { SvelteToast } from '@zerodevx/svelte-toast';

	import '../app.css';
	import Navbar from '../components/navbar/Navbar.svelte';
	import Footer from '../components/footer/Footer.svelte';
</script>

<SvelteToast />
<Navbar />
<slot />
<Footer email="ping.ayushporwal@gmail.com" />
