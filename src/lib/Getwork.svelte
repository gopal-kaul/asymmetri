<script>
    import Icon from '@iconify/svelte';
    import { form, field } from 'svelte-forms';
    import { required } from 'svelte-forms/validators';
    const name = field('name', '', [required()]);
    const email = field('email', '', [required()]);
    const description = field('description', '', [required()]);
    const experience = field('experience', '', [required()]);
    const myForm = form(name,email,description,experience);
    console.log(myForm)
	export let opengw = false;
</script>

{#if opengw}
	<div style="position: fixed; min-width: 70%; color: white;z-index:50; top: 50%; left: 50%; transform: translate(-28%, -50%)">
        <div class="h-[100vh] flex justify-center pt-12 w-full text-2xl text-center font-medium tracking-wider bg-[#1D1D1D]">
            <div>APPLY FOR A TEAM 
            <button on:click={() => {opengw=!opengw; name.reset}} class="fixed top-12 right-8" >
                <Icon icon="ic:outline-close" style="font-size:larger;color:#A8242B;" />
            </button>
        </div>
        <div class="fixed top-44 left-20 text-sm w-full">
            <section>
                <div class="grid md:grid-cols-2 md:gap-24 w-[80%]">
                    <div class="relative">
                        <input id="name" type="text" class="block py-2 px-0 w-full text-sm text-white bg-transparent border-0 border-b-2 border-gray-300 appearance-none dark:text-white dark:border-gray-600 dark:focus:border-[#A8242B] focus:outline-none focus:ring-0 focus:border-[#A8242B] peer" 
                        bind:value={$name.value} />
                        <label for="name" class="left-0 peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-focus:text-[#A8242B] peer-focus:dark:text-[#A8242B] peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">
                            Name</label>
                    </div>
                    <div class="relative">
                        <textarea id="description" type="text" class="block py-2 mt-4 rounded px-0 w-full text-sm text-black bg-white border-0 border-b-2 border-gray-300  dark:border-gray-600 dark:focus:border-[#A8242B] focus:outline-none focus:ring-0 focus:border-[#A8242B] peer" 
                        bind:value={$description.value} />
                        <label for="description" class="left-0 peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-focus:text-[#A8242B] peer-focus:dark:text-[#A8242B] peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">
                            Description</label>
                    </div>
                    <div class="relative">
                        <input id="email" type="text" class="py-2 px-0 w-full text-sm text-white bg-transparent border-0 border-b-2 border-gray-300 dark:border-gray-600  focus:outline-none focus:ring-0 focus:border-[#A8242B]" 
                        bind:value={$email.value} />
                        <label for="email" class=" left-0 peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-focus:text-[#A8242B] peer-focus:dark:text-[#A8242B] peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">
                            Email-id</label>
                    </div>
                    <div class="relative">
                        <input id="experience" placeholder="3-4 yrs." type="text" class="py-2 px-0 w-full text-sm text-white bg-transparent border-0 border-b-2 dark:border-gray-600 border-gray-300  focus:outline-none focus:ring-0 focus:border-[#A8242B]" 
                        bind:value={$experience.value} />
                        <label for="experience" class=" left-0 peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-focus:text-[#A8242B] peer-focus:dark:text-[#A8242B] peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">
                            Years of Experience</label>
                    </div>
                  </div>
                <button class="fixed justify-center h-8 w-24 rounded text-center right-[50%] bottom-0 bg-[#A8242B]" disabled={!$myForm.valid}>Submit</button>
              </section>
        </div>
        </div>
	</div>
{/if}