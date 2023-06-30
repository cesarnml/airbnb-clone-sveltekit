<script>
	import { dev } from '$app/environment';
	import { inject } from '@vercel/analytics';
	inject({ mode: dev ? 'development' : 'production' });

	import '../app.css';
	import Navbar from '$/components/navbar/Navbar.svelte';
</script>

<Navbar />
<slot />
