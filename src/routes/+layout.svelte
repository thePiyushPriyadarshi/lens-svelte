<script>
	import Footer from '../components/Footer.svelte';
import Navbar from '../components/Navbar.svelte'; 
	import './styles.css';
</script>

<div class="app dark:bg-[#000000] bg-white">
	<Navbar/>

	<main>
		<slot />
	</main>

	<Footer/>
</div>

