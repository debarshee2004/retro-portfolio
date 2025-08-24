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
				<div class="border-japanese-blue border-r"></div>
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
					<div class="bg-japanese-blue h-px flex-1"></div>
				</div>

				<!-- Title with Japanese -->
				<div class="space-y-4">
					<h2 class="brutal-title">
						<span class="japanese-kanji">私について</span><br />
						ABOUT ME
					</h2>
					<div class="brutalist-box japanese-float">
						<span class="japanese-kanji">人間</span> HUMAN
					</div>
				</div>
			</div>

			<!-- Content Grid -->
			<div class="grid grid-cols-12 gap-8 lg:gap-12">
				<!-- Main Content -->
				<div class="col-span-12 space-y-8 lg:col-span-8">
					<div class="space-y-6">
						<div class="brutalist-card">
							<p class="text-xl leading-relaxed font-light">
								I'm a backend developer and machine learning enthusiast with experience in designing
								scalable, efficient, and reliable systems. My work focuses on building <span
									class="japanese-kanji">高性能</span
								>
								backend architectures, integrating AI-powered solutions, and ensuring seamless deployment
								with modern <span class="brutal-subtitle text-sm">DevOps</span> practices.
							</p>
						</div>

						<div class="brutalist-card japanese-gold-bg text-black">
							<p class="text-lg leading-relaxed font-medium">
								When I'm not coding, I'm exploring new frameworks, contributing to <span
									class="japanese-kanji font-black">オープンソース</span
								>, or mentoring peers in backend and ML concepts. I believe in creating technology
								that empowers people and brings innovation into real-world solutions.
							</p>
						</div>
					</div>

					<!-- Philosophy Section -->
					<div class="brutal-section">
						<h3 class="brutal-subtitle mb-4">
							<span class="japanese-kanji">哲学</span> PHILOSOPHY
						</h3>
						<p class="text-sm leading-relaxed font-medium">
							Building software is like <span class="japanese-kanji">建築</span> (architecture) - it
							requires precision, planning, and attention to detail. Every line of code should serve
							a purpose, every system should be efficient, and every solution should be
							<span class="japanese-kanji">美しい</span> (beautiful) in its simplicity.
						</p>
					</div>

					<!-- Call to Action -->
					<div class="flex space-x-4">
						<a
							data-sveltekit-preload-data="hover"
							href="https://www.dinocodes.in/blogs"
							class="brutalist-button"
						>
							<span class="japanese-kanji">記事</span> READ BLOGS
						</a>
						<a href="#experience" class="brutalist-button japanese-blue-bg text-white">
							View Experience
						</a>
					</div>
				</div>

				<!-- Info Panel -->
				<div class="col-span-12 space-y-6 lg:col-span-4">
					<!-- Expertise -->
					<div class="brutalist-card japanese-red-bg w-80 text-white">
						<h3 class="brutal-subtitle mb-4 text-white">
							<span class="japanese-kanji">専門</span> EXPERTISE
						</h3>
						<div class="space-y-3">
							{#each ['Backend Development', 'Machine Learning', 'API Design', 'System Architecture', 'DevOps & Cloud'] as skill}
								<div class="flex items-center space-x-3">
									<div class="japanese-gold-bg h-3 w-3 border-2 border-black"></div>
									<span class="text-sm font-bold">{skill}</span>
								</div>
							{/each}
						</div>
					</div>

					<!-- Current Focus -->
					<div class="brutalist-card w-80">
						<h3 class="brutal-subtitle mb-3">
							<span class="japanese-kanji">現在</span> FOCUS
						</h3>
						<div class="space-y-3 text-sm">
							<div class="flex items-center justify-between">
								<span class="font-bold">AI Integration</span>
								<span class="japanese-kanji text-sm">AI統合</span>
							</div>
							<div class="flex items-center justify-between">
								<span class="font-bold">Cloud Architecture</span>
								<span class="japanese-kanji text-sm">クラウド</span>
							</div>
							<div class="flex items-center justify-between">
								<span class="font-bold">Open Source</span>
								<span class="japanese-kanji text-sm">OSS</span>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
