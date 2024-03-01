<script lang="ts">
	import { onMount } from 'svelte';
	import { cascade } from 'svelte-typewriter';
	import { quintOut } from 'svelte/easing';
	import { fade, slide } from 'svelte/transition';

	let ready = false;
	onMount(() => {
		setTimeout(() => (ready = true), 1000);
	});
</script>

<div class="flex w-full flex-grow flex-col gap-4 p-10 box-border">
	<h1 use:cascade={{ interval: 30 }} class="text-xl md:text-6xl">
		Never Compromise Your Safety Again
	</h1>

	<div
		class="flex w-full flex-grow flex-col-reverse items-center justify-between gap-8 md:flex-row"
	>
		{#if ready}
			<div
				transition:fade={{ delay: 250, duration: 500 }}
				class="flex w-full flex-col items-center justify-center gap-8 md:w-2/3 md:items-start"
			>
				<h2 class="text-balance text-center font-light md:text-left md:text-3xl">
					We build cutting-edge technology that keeps you and your loved ones safe. We scan local
					first responder radio frequency and immediately notify you of any public threats.
				</h2>

				<a
					href="/"
					class="border-2 border-black bg-white px-16 py-2 text-xl text-black transition-colors duration-300 hover:bg-black hover:text-white"
				>
					Learn More
				</a>
			</div>

			<div class="h-full w-full md:w-1/3">
				<div
					transition:slide={{ delay: 250, duration: 800, easing: quintOut, axis: 'y' }}
					class="flex h-full w-full items-center justify-center"
				>
					<img
						class="h-[500px] w-full object-contain md:h-full"
						src="render.png"
						alt="Guard AI App Render"
					/>
				</div>
			</div>
		{/if}
	</div>
</div>
