<script>
	import Navbar from '../lib/Navbar.svelte';
	import darrow from '../lib/assets/darrow.png';

	let speed = 2;
	let speed2 = 4;
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
		<h2 class="text-red-500 font-bold text-5xl px-[5%]"><span class="text-white">We build</span> awesome <br/> software!</h2>
	</div>
	<div class="h-[50vh] bg-black relative" style:transform={`translate3d(0,${scroll * speed2}px,0)`}>
		<h2 class="text-white text-2xl">
			<h2 class="text-white text-2xl pt-8 px-[5%] md:pr-[50%]">
				Most of today's problems have software <br/> solutions. We help you find and execute <br/> them - in
				style.
			</h2>
		</h2>
		<div class="absolute mt-0 ml-0">
			<button class=" bg-transparent border-white w-64 border-[1px] py-2  ml-20 mt-10 px-5 text-white absolute z-10">Get Talent</button>
			<button class=" bg-buttonRed  w-64 h-10 py-2  ml-[34.5%] mt-[17.8%] px-5 text-white relative z-1"></button>
		</div>
		<div class="mt-44 ml-[44%] text-gray-200 text-opacity-60 content flex pl-2">
		<img src={darrow} alt="arrow" class="w-4 mt-2 h-4"/>
			<span class="ml-2 font-normal">scroll down to know more</span>
	</div>
	</div>
</div>

<style>

</style>
