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
				<div class="border-retro-blue border-r"></div>
			{/each}
		</div>
	</div>

	<!-- Main Content Container -->
	<div class="relative z-10 mx-auto w-full max-w-[1600px] px-8 lg:px-16">
		<!-- Swiss Grid Layout -->
		<div class="grid grid-cols-12 gap-8 lg:gap-12">
			<!-- Left Column: Typography -->
			<div class="no-animation col-span-12 space-y-12 lg:col-span-8">
				<!-- Section Number -->
				<div class="flex items-center space-x-6">
					<div class="text-muted-foreground font-mono text-xs tracking-[0.3em] uppercase">001</div>
					<div class="bg-retro-blue h-px flex-1"></div>
				</div>

				<!-- Main Typography -->
				<div class="space-y-6">
					<h1
						class="text-6xl leading-[0.85] font-black tracking-[-0.02em] uppercase md:text-7xl lg:text-8xl"
					>
						<span class="japanese-text">建築</span><br />
						DINO<br />
						<span class="retro-blue">CODES</span>
					</h1>

					<div class="brutalist-box inline-block">
						<span class="japanese-text">職人</span> CRAFTSMAN
					</div>
				</div>

				<!-- Description -->
				<div class="max-w-2xl">
					<div class="border-retro-blue space-y-4 border-l-2 pl-6">
						<h2 class="text-xl leading-relaxed font-light lg:text-2xl">
							Backend and Machine Learning Engineer specializing in
							<span class="japanese-text">革新的</span> scalable systems and AI solutions
						</h2>
						<p class="text-muted-foreground font-mono text-sm tracking-wide">
							BUILDING THE FUTURE WITH PRECISION AND <span class="japanese-text">美学</span>
						</p>
					</div>
				</div>
			</div>

			<!-- Right Column: Info -->
			<div class="no-animation col-span-12 space-y-8 lg:col-span-4">
				<!-- Status -->
				<div class="border-foreground bg-background border-2 p-4">
					<div class="space-y-3">
						<div class="flex items-center justify-between">
							<span class="retro-blue font-mono text-xs tracking-wider uppercase">Status</span>
							<div class="flex items-center space-x-2">
								<div class="h-2 w-2 rounded-full bg-green-500"></div>
								<span class="japanese-text text-sm">利用可能</span>
							</div>
						</div>
						<div class="text-sm">Available for Projects</div>
					</div>
				</div>

				<!-- Personal Info -->
				<div class="border-retro-red space-y-3 border-l-2 pl-4">
					<div class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
						<span class="japanese-text">個人</span> PERSONAL
					</div>
					<div class="space-y-2 text-sm">
						<div class="flex justify-between">
							<span class="text-muted-foreground">Name</span>
							<span>Debarshee Chakraborty</span>
						</div>
						<div class="flex justify-between">
							<span class="text-muted-foreground">Location</span>
							<span>Kolkata, India</span>
						</div>
						<div class="flex justify-between">
							<span class="text-muted-foreground">Experience</span>
							<span class="retro-blue">2+ Years</span>
						</div>
					</div>
				</div>

				<!-- Tech Stack -->
				<div class="space-y-3">
					<div class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
						<span class="japanese-text">技術</span> STACK
					</div>
					<div class="grid grid-cols-2 gap-2 font-mono text-xs">
						<div class="border-foreground border p-2 text-center">Python</div>
						<div class="border-foreground border p-2 text-center">Java</div>
						<div class="border-foreground border p-2 text-center">Go</div>
						<div class="border-foreground border p-2 text-center">TypeScript</div>
					</div>
				</div>
			</div>
		</div>

		<!-- Bottom CTA -->
		<div class="border-retro-blue mt-16 border-t pt-8">
			<div
				class="flex flex-col items-start justify-between space-y-4 sm:flex-row sm:items-center sm:space-y-0"
			>
				<p class="text-muted-foreground font-mono text-sm">
					Ready to build something <span class="japanese-text">素晴らしい</span>?
				</p>
				<div class="flex space-x-4">
					<a href="#contact" class="brutalist-box no-underline">
						<span class="japanese-text">連絡</span> CONTACT
					</a>
					<a
						href="#experience"
						class="border-foreground hover:bg-foreground hover:text-background border px-4 py-2 font-mono text-xs uppercase transition-colors"
					>
						View Work
					</a>
				</div>
			</div>
		</div>
	</div>
</section>
