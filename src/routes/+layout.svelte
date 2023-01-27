<script>
	import '../app.css';
	import Navbar from '../lib/Navbar.svelte';
	import Vision from '../lib/Vision.svelte';
</script>

<div>
	<Navbar />
</div>
<div class="">
	<slot/>
	<Vision/>
</div>
