<script lang="ts">
	const currentYear = new Date().getFullYear();
</script>

<footer class="border-foreground/20 relative mt-24 border-t pt-16">
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
				<!-- Title with Japanese -->
				<div class="space-y-4">
					<h2 class="brutal-title">
						<span class="japanese-kanji">終了</span> FOOTER
					</h2>
					<div class="brutalist-box japanese-float">
						<span class="japanese-kanji">さようなら</span> SAYONARA
					</div>
				</div>
			</div>

			<!-- Footer Content -->
			<div class="brutal-grid grid-cols-1 gap-12 lg:grid-cols-2">
				<!-- Main Message -->
				<div class="brutal-section">
					<h3 class="brutal-subtitle mb-4">Let's Build Something Amazing Together</h3>
					<p class="text-base leading-relaxed font-medium">
						I'm always interested in new opportunities and exciting projects. Let's connect and
						create something <span class="japanese-kanji">素晴らしい</span>.
					</p>
				</div>
			</div>

			<!-- Bottom Section -->
			<div class="japanese-border mt-12 p-6">
				<div class="flex flex-col space-y-4 md:flex-row md:justify-between md:space-y-0">
					<div class="brutal-subtitle text-sm">
						© {currentYear} Debarshee Chakraborty. All rights reserved.
					</div>
					<div class="brutal-subtitle text-sm">
						<span class="japanese-kanji">作成者</span> CRAFTED WITH LOVE
					</div>
				</div>
			</div>
		</div>
	</div>
</footer>
