<script lang="ts">
	let mounted = false;

	import { onMount } from 'svelte';

	onMount(() => {
		mounted = true;
	});
</script>

<section id="hero" class="relative flex min-h-screen items-center">
	<!-- Simple Grid Overlay -->
	<div class="pointer-events-none absolute inset-0 opacity-5">
		<div class="grid h-full grid-cols-12 gap-8">
			{#each Array(12) as _, i}
				<div class="border-japanese-blue border-r"></div>
			{/each}
		</div>
	</div>

	<!-- Main Content Container -->
	<div class="relative z-10 mx-auto w-full max-w-[1600px] px-4 sm:px-6 md:px-8 lg:px-16">
		<!-- Swiss Grid Layout -->
		<div class="grid grid-cols-12 gap-4 sm:gap-6 md:gap-8 lg:gap-12">
			<!-- Left Column: Typography -->
			<div class="no-animation col-span-12 space-y-6 sm:space-y-8 md:space-y-12 lg:col-span-8">
				<!-- Section Number -->
				<div class="flex items-center space-x-6">
					<div class="text-muted-foreground font-mono text-xs tracking-[0.3em] uppercase">001</div>
					<div class="bg-retro-blue h-px flex-1"></div>
				</div>

				<!-- Main Typography -->
				<div class="space-y-6">
					<h1 class="brutal-title">
						<span class="japanese-kanji">建築家</span><br />
						DINO<br />
						<span class="japanese-blue">CODES</span>
					</h1>

					<div class="brutalist-box japanese-float">
						<span class="japanese-kanji">職人</span> DIGITAL CRAFTSMAN
					</div>
				</div>

				<!-- Description -->
				<div class="max-w-2xl">
					<div class="brutalist-card">
						<h2 class="text-xl leading-relaxed font-light lg:text-2xl">
							Backend and Machine Learning Engineer specializing in
							<span class="japanese-kanji">革新的</span> scalable systems and AI solutions
						</h2>
						<p class="text-muted-foreground mt-4 font-mono text-sm tracking-wide">
							BUILDING THE FUTURE WITH PRECISION AND <span class="japanese-kanji">美学</span>
						</p>
					</div>
				</div>
			</div>

			<!-- Right Column: Info -->
			<div
				class="no-animation col-span-12 mt-8 space-y-4 sm:space-y-6 md:space-y-8 lg:col-span-4 lg:mt-0"
			>
				<!-- Status -->
				<div class="brutalist-card">
					<div class="space-y-3">
						<div class="flex items-center justify-between">
							<span class="brutal-subtitle text-xs">Status</span>
							<div class="flex items-center space-x-2">
								<div class="bg-japanese-green border-japanese-black h-3 w-3 border-2"></div>
								<span class="japanese-kanji text-sm">利用可能</span>
							</div>
						</div>
						<div class="text-sm font-bold">Available for Projects</div>
					</div>
				</div>

				<!-- Personal Info -->
				<div class="brutalist-card japanese-red-bg w-80 text-white">
					<div class="brutal-subtitle mb-3">
						<span class="japanese-kanji">個人</span> PERSONAL
					</div>
					<div class="space-y-2 text-sm">
						<div class="flex items-center justify-between">
							<span class="font-mono">Name</span>
							<span class="font-bold">Debarshee Chakraborty</span>
						</div>
						<div class="flex items-center justify-between">
							<span class="font-mono">Location</span>
							<span class="font-bold">Kolkata, India</span>
						</div>
						<div class="flex items-center justify-between">
							<span class="font-mono">Experience</span>
							<span class="brutal-subtitle ml-2 text-xs">2+ Years</span>
						</div>
					</div>
				</div>

				<!-- Tech Stack -->
				<div class="space-y-3">
					<div class="brutal-subtitle">
						<span class="japanese-kanji">技術</span> STACK
					</div>
					<div class="brutal-grid grid-cols-2 gap-2">
						<div class="brutalist-button text-center text-xs">Python</div>
						<div class="brutalist-button japanese-gold-bg text-center text-xs text-black">Java</div>
						<div class="brutalist-button japanese-red-bg text-center text-xs">Go</div>
						<div class="brutalist-button text-center text-xs">TypeScript</div>
					</div>
				</div>
			</div>
		</div>

		<!-- Bottom CTA -->
		<div class="japanese-border mt-8 p-4 sm:mt-12 sm:p-6 md:mt-16 md:p-8">
			<div
				class="flex flex-col items-start justify-between space-y-4 sm:flex-row sm:items-center sm:space-y-0"
			>
				<p class="brutal-subtitle text-center sm:text-left">
					Ready to build something <span class="japanese-kanji">素晴らしい</span>?
				</p>
				<div class="flex w-full flex-col space-y-2 sm:w-auto sm:flex-row sm:space-y-0 sm:space-x-4">
					<a href="#contact" class="brutalist-button text-center">
						<span class="japanese-kanji">連絡</span> CONTACT
					</a>
					<a href="#experience" class="brutalist-button japanese-blue-bg text-center text-white">
						View Work
					</a>
				</div>
			</div>
		</div>
	</div>
</section>
