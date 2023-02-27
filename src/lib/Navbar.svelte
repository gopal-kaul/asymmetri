<script>
	// Logo import
	import logo from '$lib/assets/logo.png';
	import Overlay from './assets/Overlay.svelte';
	import Getwork from './Getwork.svelte';
	function getwork(){
		console.log("Clicked Get Work!");
	}
	let opengw = false;
</script>
	<div class="flex flex-row items-center justify-between w-full bg-black px-[5.2%] fixed top-0 py-[2%] z-50">
		<div>
			<img src={logo} alt="Asymmetri" class="w-[15vw] h-auto" />
	</div>
	<div class="flex flex-row gap-4 items-center">
		<button class="bg-buttonRed py-2 px-5 text-white relative z-10">Get Talent</button>
		<button  on:click={() => {console.log("openclicked"); opengw = !opengw; opengw = true}} class="bg-buttonRed py-2 px-5 text-white relative z-10">Get Work</button>
		<Overlay class="z-50">
			<Getwork {opengw} />
		</Overlay>
		<button class="bg-buttonRed py-2 px-5 text-white relative z-10">Post an Idea</button>
	</div>
	
</div>

<style>
	button::before {
		content: '';
		position: absolute;
		width: 104%;
		height: 100%;
		top: 5px;
		left: -5px;
		background-color: inherit;
		z-index: -1;
	}
</style>
