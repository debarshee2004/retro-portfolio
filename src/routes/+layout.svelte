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
		class="bg-background text-foreground relative mx-auto min-h-screen max-w-6xl px-4 py-8 font-sans antialiased sm:px-6 sm:py-12 md:px-8 md:py-16 lg:px-16"
	>
		<!-- Corner decorative elements - Mobile responsive -->
		<div class="fixed top-2 left-2 z-50 hidden sm:top-4 sm:left-4 sm:block">
			<div class="brutalist-box text-xs">
				<span class="japanese-kanji">建</span>
			</div>
		</div>

		<div class="fixed top-2 right-2 z-50 hidden sm:top-4 sm:right-4 sm:block">
			<div class="brutalist-box text-xs">
				<span class="japanese-kanji">築</span>
			</div>
		</div>

		{@render children()}
	</div>

	<!-- Bottom Japanese accent line -->
	<!-- <div class="japanese-accent-line"></div> -->
</div>
