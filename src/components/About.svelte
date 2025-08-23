<script lang="ts">
	let mounted = false;

	import { onMount } from 'svelte';

	onMount(() => {
		mounted = true;
	});
</script>

<section id="about" class="no-animation relative">
	<!-- Simple Grid Overlay -->
	<div class="pointer-events-none absolute inset-0 opacity-5">
		<div class="grid h-full grid-cols-12 gap-8">
			{#each Array(12) as _, i}
				<div class="border-retro-blue border-r"></div>
			{/each}
		</div>
	</div>

	<div class="relative z-10 mx-auto w-full max-w-[1600px] px-8 lg:px-16">
		<div class="space-y-16">
			<!-- Header -->
			<div class="space-y-8">
				<!-- Section Number -->
				<div class="flex items-center space-x-6">
					<div class="text-muted-foreground font-mono text-xs tracking-[0.3em] uppercase">002</div>
					<div class="bg-retro-blue h-px flex-1"></div>
				</div>

				<!-- Title with Japanese -->
				<div class="space-y-4">
					<h2 class="text-6xl font-black tracking-[-0.02em] uppercase md:text-7xl">
						<span class="japanese-text">について</span><br />
						ABOUT
					</h2>
					<div class="brutalist-box inline-block">
						<span class="japanese-text">私</span> MYSELF
					</div>
				</div>
			</div>

			<!-- Content Grid -->
			<div class="grid grid-cols-12 gap-8 lg:gap-12">
				<!-- Main Content -->
				<div class="col-span-12 space-y-8 lg:col-span-8">
					<div class="space-y-6">
						<p class="text-xl leading-relaxed font-light">
							I'm a backend developer and machine learning enthusiast with experience in designing
							scalable, efficient, and reliable systems. My work focuses on building <span
								class="japanese-text">高性能</span
							>
							backend architectures, integrating AI-powered solutions, and ensuring seamless deployment
							with modern <span class="retro-blue font-medium">DevOps</span> practices.
						</p>

						<p class="text-muted-foreground text-lg leading-relaxed font-light">
							When I'm not coding, I'm exploring new frameworks, contributing to <span
								class="japanese-text">オープンソース</span
							>, or mentoring peers in backend and ML concepts. I believe in creating technology
							that empowers people and brings innovation into real-world solutions.
						</p>
					</div>

					<!-- Philosophy Section -->
					<div class="border-foreground bg-background border-2 p-6">
						<h3 class="retro-blue mb-4 font-mono text-sm tracking-wider uppercase">
							<span class="japanese-text">哲学</span> PHILOSOPHY
						</h3>
						<p class="text-sm leading-relaxed">
							Building software is like <span class="japanese-text">建築</span> (architecture) - it
							requires precision, planning, and attention to detail. Every line of code should serve
							a purpose, every system should be efficient, and every solution should be
							<span class="japanese-text">美しい</span> (beautiful) in its simplicity.
						</p>
					</div>

					<!-- Call to Action -->
					<div class="flex space-x-4">
						<a data-sveltekit-preload-data="hover" href="/blogs" class="brutalist-box no-underline">
							<span class="japanese-text">記事</span> READ BLOGS
						</a>
						<a
							href="#experience"
							class="border-retro-blue hover:bg-retro-blue hover:text-background border px-6 py-3 font-mono text-sm uppercase transition-colors"
						>
							View Experience
						</a>
					</div>
				</div>

				<!-- Info Panel -->
				<div class="col-span-12 space-y-6 lg:col-span-4">
					<!-- Expertise -->
					<div class="border-retro-red border-l-2 pl-4">
						<h3 class="text-muted-foreground mb-4 font-mono text-sm tracking-wider uppercase">
							<span class="japanese-text">専門</span> EXPERTISE
						</h3>
						<div class="space-y-2">
							{#each ['Backend Development', 'Machine Learning', 'API Design', 'System Architecture', 'DevOps & Cloud'] as skill}
								<div class="flex items-center space-x-2">
									<div class="bg-retro-blue h-1 w-1"></div>
									<span class="text-sm">{skill}</span>
								</div>
							{/each}
						</div>
					</div>

					<!-- Current Focus -->
					<div class="border-foreground bg-background border p-4">
						<h3 class="retro-yellow mb-3 font-mono text-sm tracking-wider uppercase">
							<span class="japanese-text">現在</span> FOCUS
						</h3>
						<div class="space-y-2 text-sm">
							<div class="flex justify-between">
								<span>AI Integration</span>
								<span class="japanese-text text-xs">AI統合</span>
							</div>
							<div class="flex justify-between">
								<span>Cloud Architecture</span>
								<span class="japanese-text text-xs">クラウド</span>
							</div>
							<div class="flex justify-between">
								<span>Open Source</span>
								<span class="japanese-text text-xs">OSS</span>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
