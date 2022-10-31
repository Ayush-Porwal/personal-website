<script>
	import '../app.css';
	import Navbar from '../components/navbar/Navbar.svelte';
	import Footer from '../components/footer/Footer.svelte';
</script>

<Navbar />
<slot />
<Footer email="ping.ayushporwal@gmail.com" />
