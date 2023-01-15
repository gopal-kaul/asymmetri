<script>
	// Logo import
	import logo from '$lib/assets/logo.png';
</script>

<div class="flex flex-row items-center justify-between w-full bg-black px-[5%] fixed top-0">
	<div>
		<img src={logo} alt="Asymmetri" class="" />
	</div>
	<div class="flex flex-row gap-4 items-center">
		<button class="bg-buttonRed py-2 px-5 text-white relative z-10">Get Talent</button>
		<button class="bg-buttonRed py-2 px-5 text-white relative z-10">Get Work</button>
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
