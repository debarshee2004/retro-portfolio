<script lang="ts">
	const currentYear = new Date().getFullYear();
</script>

<footer class="border-foreground/20 relative mt-24 border-t pt-16">
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
				<!-- Title with Japanese -->
				<div class="space-y-4">
					<h2 class="brutal-title text-4xl md:text-6xl">
						<span class="japanese-kanji">終了</span> FOOTER
					</h2>
					<div class="brutalist-box japanese-float">
						<span class="japanese-kanji">さようなら</span> SAYONARA
					</div>
				</div>

				<!-- Quirky Fun Elements -->
				<div class="mt-8 grid grid-cols-1 gap-4 md:grid-cols-3">
					<!-- Fun Fact 1 -->
					<div class="brutalist-card-blue text-center">
						<div class="japanese-kanji mb-2 text-2xl">🚀</div>
						<p class="text-xs font-bold">
							POWERED BY<br /><span class="japanese-kanji">情熱</span> PASSION
						</p>
					</div>

					<!-- Fun Fact 2 -->
					<div class="brutalist-card japanese-gold-bg text-center text-black">
						<div class="mb-2 text-2xl">⚡</div>
						<p class="text-xs font-bold">
							MADE WITH<br /><span class="japanese-kanji">愛</span> LOVE & COFFEE
						</p>
					</div>

					<!-- Fun Fact 3 -->
					<div class="brutalist-card japanese-red-bg text-center text-white">
						<div class="japanese-kanji mb-2 text-2xl">🎯</div>
						<p class="text-xs font-bold">
							BUILDING<br /><span class="japanese-kanji">未来</span> THE FUTURE
						</p>
					</div>
				</div>

				<!-- ASCII Art Section -->
				<div
					class="brutalist-card japanese-black-bg text-japanese-gold hidden text-center md:block lg:flex"
				>
					<pre class="font-mono text-xs leading-tight">
						THANK YOU FOR VISITING!
						また会いましょう
						(See you again!)
					</pre>
				</div>
			</div>

			<!-- Footer Content -->
			<div class="grid grid-cols-1 gap-8 lg:grid-cols-2 lg:gap-12">
				<!-- Main Message -->
				<div class="brutal-section">
					<h3 class="brutal-subtitle mb-4 text-base md:text-lg">
						Let's Build Something Amazing Together
					</h3>
					<p class="text-sm leading-relaxed font-medium md:text-base">
						I'm always interested in new opportunities and exciting projects. Let's connect and
						create something <span class="japanese-kanji">素晴らしい</span>.
					</p>
				</div>

				<!-- Contact & Links -->
				<div class="grid grid-cols-1 gap-6 sm:grid-cols-2">
					<!-- Quick Links -->
					<div class="brutalist-card">
						<h4 class="brutal-subtitle mb-4 text-sm">
							<span class="japanese-kanji">リンク</span> LINKS
						</h4>
						<div class="space-y-3">
							<a
								target="_blank"
								href="https://github.com/debarshee2004"
								class="brutalist-button block w-full text-center text-xs"
							>
								GitHub Projects
							</a>
							<a
								data-sveltekit-preload-data="hover"
								href="/blogs"
								class="brutalist-button japanese-blue-bg block w-full text-center text-xs text-white"
							>
								Tech Blogs
							</a>
							<a
								data-sveltekit-preload-data="hover"
								href="/links"
								class="brutalist-button japanese-gold-bg block w-full text-center text-xs text-black"
							>
								All Links
							</a>
						</div>
					</div>

					<!-- Tech Stack -->
					<div class="brutalist-card japanese-red-bg text-white">
						<h4 class="brutal-subtitle mb-4 text-sm text-white">
							<span class="japanese-kanji">技術</span> BUILT WITH
						</h4>
						<div class="space-y-2 text-xs font-bold">
							<div class="flex items-center justify-between">
								<span>SvelteKit</span>
								<span class="japanese-kanji">⚡</span>
							</div>
							<div class="flex items-center justify-between">
								<span>Tailwind CSS</span>
								<span class="japanese-kanji">🎨</span>
							</div>
							<div class="flex items-center justify-between">
								<span>TypeScript</span>
								<span class="japanese-kanji">📝</span>
							</div>
							<div class="flex items-center justify-between">
								<span>Cloudflare</span>
								<span class="japanese-kanji">☁️</span>
							</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Bottom Section -->
			<div class="japanese-border mt-12 p-4 md:p-6">
				<div
					class="flex flex-col items-center space-y-4 md:flex-row md:justify-between md:space-y-0"
				>
					<div class="brutal-subtitle text-center text-xs md:text-left md:text-sm">
						© {currentYear} Debarshee Chakraborty. All rights reserved.
					</div>
					<div class="brutal-subtitle text-center text-xs md:text-right md:text-sm">
						<span class="japanese-kanji">作成者</span> CRAFTED WITH LOVE
					</div>
				</div>

				<!-- Mobile ASCII Art -->
				<div class="brutalist-card japanese-black-bg text-japanese-gold mt-4 text-center md:hidden">
					<div class="text-sm">
						<span class="japanese-kanji">🙏</span> ありがとう
						<span class="japanese-kanji">🙏</span><br />
						<span class="text-xs">THANK YOU!</span>
					</div>
				</div>
			</div>
		</div>
	</div>
</footer>
