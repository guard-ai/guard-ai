<script>
	import '../app.css';
</script>

<div class="flex h-full w-full flex-col items-center justify-center">
	<div class="flex h-full w-full max-w-[1440px] flex-col items-start p-8 box-border">
		<div class="flex w-full flex-row p-10 box-border">
			<div class="flex flex-grow flex-row items-center gap-2">
				<a href="/">
					<img class="h-8 w-8" src="/logo.png" alt="logo" />
				</a>
				<h1 class="text-lg md:text-2xl">Guard AI</h1>
			</div>

			<div class="flex flex-grow-0 flex-row items-center gap-4">
				<a class="text-base font-light hover:underline md:text-xl" href="/about">About</a>
				<a class="text-base font-light hover:underline md:text-xl" href="/team">Team</a>
			</div>
		</div>

		<slot />

		<div class="flex w-full flex-grow-0 flex-row p-10 box-border">
			<div class="flex flex-grow flex-row gap-4">
				<a class="md:text-md text-xs font-light text-gray-500 hover:underline" href="/"
					>PRIVACY POLICY</a
				>
				<a class="md:text-md text-xs font-light text-gray-500 hover:underline" href="/"
					>TERMS OF SERVICE</a
				>
			</div>
			<div class="flex flex-grow-0 flex-row gap-4">
				<p class="md:text-md text-xs font-light text-gray-500">COPYRIGHT 2024 GUARD AI</p>
				<p class="md:text-md text-xs font-light text-gray-500">ALL RIGHTS RESERVED</p>
			</div>
		</div>
	</div>
</div>
