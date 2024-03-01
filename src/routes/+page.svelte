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

<div class="flex h-full w-full flex-col items-center justify-center">
	<div class="flex h-full w-full max-w-[1440px] flex-col items-start p-8">

		<div class="flex w-full flex-row p-2">
			<div class="flex flex-grow flex-row items-center gap-2">
				<a href="/">
					<img class="h-8 w-8" src="/logo.png" alt="logo" />
				</a>
				<h1 class="text-lg md:text-2xl">Guard AI</h1>
			</div>

			<div class="flex flex-grow-0 flex-row items-center gap-4">
				<a class="text-base md:text-xl font-light hover:underline" href="/">About</a>
				<a class="text-base md:text-xl font-light hover:underline" href="/">Contact</a>
				<a class="text-base md:text-xl font-light hover:underline" href="/">Team</a>
			</div>
		</div>

		<div class="flex flex-grow w-full flex-col gap-4 p-8">
			<h1 use:cascade={{ interval: 30 }} class="text-xl md:text-6xl">
				Never Compromise Your Safety Again
			</h1>

			<div
				class="flex flex-grow w-full flex-col-reverse items-center justify-between gap-8 md:flex-row"
			>
				{#if ready}
					<div
						transition:fade={{ delay: 250, duration: 500 }}
						class="flex w-full flex-col items-center md:items-start justify-center gap-8 md:w-2/3"
					>
						<h2 class="text-balance text-center md:text-left font-light md:text-3xl">
							We build cutting-edge technology that keeps you and your loved ones safe. We scan
							local first responder radio frequency and immediately notify you of any public
							threats.
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
								class="h-[500px] md:h-full w-full object-contain"
								src="render.png"
								alt="Guard AI App Render"
							/>
						</div>
					</div>
				{/if}
			</div>
		</div>

		<div class="flex flex-grow-0 w-full flex-row p-4">
			<div class="flex flex-grow flex-row gap-4">
				<a class="text-xs md:text-md font-light text-gray-500 hover:underline" href="/">PRIVACY POLICY</a>
				<a class="text-xs md:text-md font-light text-gray-500 hover:underline" href="/">TERMS OF SERVICE</a>
			</div>
			<div class="flex flex-grow-0 flex-row gap-4">
				<p class="text-xs md:text-md font-light text-gray-500">COPYRIGHT 2024 GUARD AI</p>
				<p class="text-xs md:text-md font-light text-gray-500">ALL RIGHTS RESERVED</p>
			</div>
		</div>
	</div>
</div>
