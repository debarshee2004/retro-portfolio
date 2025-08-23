<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<svelte:head>
	<!-- Japanese font imports -->
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" />
	<link
		href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700;900&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<!-- Japanese brutalist wrapper with decorative elements -->
<div class="japanese-dot-pattern min-h-screen">
	<!-- Top Japanese accent line -->
	<!-- <div class="japanese-accent-line"></div> -->

	<div
		class="bg-background text-foreground relative mx-auto min-h-screen max-w-6xl px-8 py-16 font-sans antialiased lg:px-16"
	>
		<!-- Corner decorative elements -->
		<!-- <div class="fixed top-4 left-4 z-50">
			<div class="brutalist-box text-xs">
				<span class="japanese-kanji">建</span>
			</div>
		</div>

		<div class="fixed top-4 right-4 z-50">
			<div class="brutalist-box text-xs">
				<span class="japanese-kanji">築</span>
			</div>
		</div> -->

		{@render children()}
	</div>

	<!-- Bottom Japanese accent line -->
	<!-- <div class="japanese-accent-line"></div> -->
</div>
