<script>
	import Navbar from '../lib/Navbar.svelte';

	let speed = 3;
	let scroll;
</script>

<svelte:window bind:scrollY={scroll} />
<div class="h-screen">
	<Navbar />
	<div class="h-screen" />
</div>
<div class="absolute top-0 left-0 w-full h-[100.1vh]">
	<div
		class="h-[50vh] bg-black flex flex-col justify-between"
		style:transform={`translate3d(0,-${scroll * speed}px,0)`}
	>
		<Navbar />
		<div class="" />
		<h2 class="text-red-500 font-bold text-5xl px-[5%]">We build awesome <br />software</h2>
	</div>
	<div class="h-[50vh] bg-black" style:transform={`translate3d(0,${scroll * speed}px,0)`}>
		<h2 class="text-white text-2xl">
			<h2 class="text-white text-4xl px-[5%] md:pr-[50%]">
				Most of today's problems have software solutions. We help you find and execute them - in
				style.
			</h2>
		</h2>
	</div>
</div>

<style>
</style>
