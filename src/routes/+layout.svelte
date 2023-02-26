<script>
	import '../app.css';
	import Navbar from '../lib/Navbar.svelte';
	import Vision from '../lib/Vision.svelte';

	let hideScroll = true;
</script>
<body class:hideScroll id="scrollingBlock">
<div class="">
	<Navbar />
</div>
<div class="">
	<slot/>
	<Vision/>
</div>
</body>
<style>
	.hideScroll::-webkit-scrollbar { display: none; }
	.hidescroll {  /* IE and Edge */
  	scrollbar-width: none;     /* Firefox */
	}
	.spacer { height: 10vh; }
	#scrollingBlock {
		border: 2px solid black;
		/*box-shadow: 10px 5px 5px red;*/
		overflow-y: scroll;
	}
</style>
