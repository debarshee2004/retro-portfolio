<script lang="ts">
	const currentYear = new Date().getFullYear();
</script>

<footer class="border-foreground/20 mt-24 border-t pt-16">
	<div class="space-y-12">
		<!-- Header with Japanese -->
		<div class="mb-12">
			<h2 class="mb-4 text-3xl font-bold">
				<span class="japanese-text">終わり</span> Footer
			</h2>
		</div>

		<!-- Footer Content -->
		<div class="grid grid-cols-1 gap-12 lg:grid-cols-2">
			<!-- Main Message -->
			<div class="brutalist-box">
				<h3 class="mb-4 text-xl font-bold tracking-wide uppercase">
					Let's Build Something Amazing Together
				</h3>
				<p class="text-muted-foreground leading-relaxed">
					I'm always interested in new opportunities and exciting projects. Let's connect and create
					something extraordinary.
				</p>
			</div>

			<!-- Links & Info -->
			<div class="grid grid-cols-1 gap-8 md:grid-cols-2">
				<!-- Quick Links -->
				<div>
					<h4 class="text-retro-blue mb-4 text-sm font-bold tracking-wide uppercase">
						Quick Links
					</h4>
					<div class="space-y-2">
						<a
							target="_blank"
							href="https://github.com/debarshee2004"
							class="hover:text-retro-blue block text-sm transition-colors"
						>
							→ Projects
						</a>
						<a
							data-sveltekit-preload-data="hover"
							href="/blogs"
							class="hover:text-retro-blue block text-sm transition-colors"
						>
							→ Blogs
						</a>
						<a
							data-sveltekit-preload-data="hover"
							href="/links"
							class="hover:text-retro-blue block text-sm transition-colors"
						>
							→ Links
						</a>
					</div>
				</div>

				<!-- Tech Stack -->
				<div>
					<h4 class="text-retro-blue mb-4 text-sm font-bold tracking-wide uppercase">Built With</h4>
					<div class="text-muted-foreground space-y-1 text-sm">
						<div>SvelteKit</div>
						<div>Tailwind CSS</div>
						<div>TypeScript</div>
						<div>Cloudflare</div>
					</div>
				</div>
			</div>
		</div>

		<!-- Bottom Section -->
		<div class="border-foreground/20 border-t pt-8">
			<div class="flex flex-col space-y-4 md:flex-row md:justify-between md:space-y-0">
				<div class="text-muted-foreground text-sm">
					© {currentYear} Debarshee Chakraborty. All rights reserved.
				</div>
				<div class="text-muted-foreground text-sm">Designed with Swiss typography principles</div>
			</div>
		</div>
	</div>
</footer>
