<script>
	import Navbar from '../lib/Navbar.svelte';
	import darrow from '../lib/assets/darrow.png';
	import Vector0 from '$lib/assets/Vector0.png';
	import Vector1 from '$lib/assets/Vector1.png';
	import Vision from '../lib/Vision.svelte';

	let top_speed = 1;
	let bottom_speed = 3;
	let scroll;
</script>
<svelte:window bind:scrollY={scroll} />

<div class="h-screen">
	<Navbar />
	<div class="bg-buttonRed h-full ml-44 w-[10px] -z-10"
	style:transform={`translate3d(0,${scroll * 0.5}px,0)`}></div>
	<img src={Vector0} alt="Asymmetri" class="w-[28vw] ml-4 -mb-96 -mt-44 h-[80vh] -z-50" 
	style:transform={`translate3d(0,${scroll * 0.1}px,0)`}/>
	<div class="bg-buttonRed ml-20 h-full w-[5px]"
	style:transform={`translate3d(0,${scroll * -0.1}px,0)`}></div>
	<div class="absolute bg-buttonRed bottom-0 right-4 h-full w-[5px]"
	style:transform={`translate3d(0,${scroll * 0.4}px,0)`}></div>
	<div class="absolute bg-buttonRed bottom-0 right-32 h-full w-[10px]"
	style:transform={`translate3d(0,${scroll * 1.9}px,0)`}></div>
	<div class="h-screen" />
	
</div>
<div class="absolute top-0 left-0 w-full h-[100.1vh] z-50">
	<div
		class="h-[50vh] bg-black flex flex-col justify-between"
		style:transform={`translate3d(0,-${scroll * top_speed}px,0)`}
	>
		<Navbar />
		<div class="" />
		<h2 class="text-red-500 font-bold text-5xl px-[5%] z-50"><span class="text-white">We build</span> awesome <br/> software!</h2>
	</div>
	<div class="h-[50vh] bg-black relative" style:transform={`translate3d(0,${scroll * bottom_speed}px,0)`}>
		<h2 class="text-white text-2xl">
			<h2 class="text-white text-2xl pt-8 px-[5%] md:pr-[50%]">
				Most of today's problems have software <br/> solutions. We help you find and execute <br/> them - in
				style.
			</h2>
		</h2>
		<div class="absolute mt-0 ml-0">
			<button class=" bg-transparent border-white w-64 border-[1px] py-2  ml-20 mt-10 px-5 text-white absolute z-10">Let's Connect</button>
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
