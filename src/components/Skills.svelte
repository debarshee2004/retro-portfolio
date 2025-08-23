<script lang="ts">
	import skillsData from '../data/skills.json';

	let skills: any[] = skillsData;
</script>

<section id="skills" class="no-animation relative">
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
					<div class="text-muted-foreground font-mono text-xs tracking-[0.3em] uppercase">004</div>
					<div class="bg-retro-blue h-px flex-1"></div>
				</div>

				<!-- Title with Japanese -->
				<div class="space-y-4">
					<h2 class="brutal-title">
						<span class="japanese-kanji">技術力</span><br />
						SKILLS
					</h2>
					<div class="brutalist-box japanese-float">
						<span class="japanese-kanji">職人技</span> CRAFTSMANSHIP
					</div>
				</div>
			</div>

			<!-- Skills Categories -->
			<div class="space-y-16">
				{#each skills as category}
					<div class="space-y-8">
						<!-- Category Header -->
						<div class="brutal-section">
							<div class="mb-4 flex items-center space-x-4">
								<h3 class="brutal-subtitle">
									{category.category}
								</h3>
								<div class="japanese-accent-line flex-1"></div>
							</div>

							{#if category.japaneseCategory}
								<div class="japanese-kanji mb-3 text-lg font-bold">
									{category.japaneseCategory}
								</div>
							{/if}

							{#if category.philosophy}
								<div class="brutalist-card japanese-gold-bg text-black">
									<p class="text-sm font-bold">
										Philosophy: <span class="japanese-kanji">{category.philosophy}</span>
									</p>
								</div>
							{/if}
						</div>

						<!-- Skills Grid -->
						<div class="brutal-grid">
							{#each category.skills as skill}
								<div class="brutalist-card">
									<div class="space-y-3">
										<div class="flex items-start justify-between">
											<div class="text-sm leading-relaxed font-bold">{skill.name}</div>
										</div>

										{#if skill.level}
											<div class="flex items-center space-x-3">
												<div class="japanese-kanji text-xs font-bold">
													{skill.level}
												</div>
												<div class="japanese-accent-line flex-1"></div>
											</div>
										{/if}
									</div>
								</div>
							{/each}
						</div>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>
