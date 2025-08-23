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
					<h2 class="text-6xl font-black tracking-[-0.02em] uppercase md:text-7xl">
						<span class="japanese-text">技術</span><br />
						SKILLS
					</h2>
					<div class="brutalist-box inline-block">
						<span class="japanese-text">職人</span> CRAFTSMANSHIP
					</div>
				</div>
			</div>

			<!-- Skills Categories -->
			<div class="space-y-16">
				{#each skills as category}
					<div class="space-y-8">
						<!-- Category Header -->
						<div class="space-y-4">
							<div class="flex items-center space-x-4">
								<h3 class="text-2xl font-bold tracking-wide uppercase">
									{category.category}
								</h3>
								<div class="bg-retro-blue h-px flex-1"></div>
							</div>

							{#if category.japaneseCategory}
								<div class="japanese-text text-lg font-medium">
									{category.japaneseCategory}
								</div>
							{/if}

							{#if category.philosophy}
								<div class="border-retro-yellow border-l-2 pl-4">
									<p class="text-muted-foreground text-sm font-light italic">
										Philosophy: <span class="japanese-text">{category.philosophy}</span>
									</p>
								</div>
							{/if}
						</div>

						<!-- Skills Grid -->
						<div class="grid grid-cols-1 gap-6 md:grid-cols-2 xl:grid-cols-3">
							{#each category.skills as skill}
								<div
									class="border-foreground group hover:border-retro-blue border-2 p-6 transition-all"
								>
									<div class="space-y-3">
										<div class="flex items-start justify-between">
											<div class="text-sm leading-relaxed font-medium">{skill.name}</div>
											{#if skill.years}
												<div class="text-retro-blue font-mono text-xs tracking-wider uppercase">
													{skill.years}
												</div>
											{/if}
										</div>

										{#if skill.level}
											<div class="flex items-center space-x-3">
												<div class="japanese-text text-xs font-medium">
													{skill.level}
												</div>
												<div
													class="bg-retro-blue h-px flex-1 opacity-30 transition-opacity group-hover:opacity-100"
												></div>
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
