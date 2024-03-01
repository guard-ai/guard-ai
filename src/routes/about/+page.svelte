<script lang="ts">
	import { concurrent } from 'svelte-typewriter';
</script>

<div class="flex w-full flex-grow flex-col gap-4 p-8">
	<h1 use:concurrent={{ interval: 30 }} class="pt-8 text-xl md:text-6xl">
		AI Powered Mission To Save Lives
	</h1>

	<div class="w-full bg-gray-50 p-8">
		<p class="text-base font-light">
			Guard AI’s real-time alert system helps keep users safe from threats even before the news
			reports on them. Get notified the moment first responders are dispatched. Alerts come from
			original sources of truth, so no more crowd-sourced, confusing information when your safety is
			on the line. At scale, this puts public safety back into your hands.
		</p>
	</div>

	<div class="flex w-full flex-row justify-center py-8">
		<img class="w-[500px]" src="/about/demo.png" alt="avalance demo" />
	</div>

	<div class="flex w-full flex-col px-32">
		<p class="">
			Guard AI notified me an avalance was ocurring the moment the NOAA dispatched a warning. We
			took cover before a Wireless Emergency Alert (WEA) was even broadcasted
		</p>

		<div class="flex w-full flex-row items-center justify-end gap-2">
			<p class="">- Veronica Baker</p>
			<img
				class="h-12 w-12 rounded-full"
				src="/about/veronica.jpeg"
				alt="veronica skiing with others"
			/>
		</div>
	</div>
</div>
