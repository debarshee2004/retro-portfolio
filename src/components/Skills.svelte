<script lang="ts">
	import skillsData from '../data/skills.json';

	let skills: any[] = skillsData;
</script>

<section id="skills" class="no-animation relative">
	<!-- Section Number -->
	<div class="mb-12 flex items-center space-x-6">
		<div class="text-muted-foreground font-mono text-xs tracking-[0.3em] uppercase">004</div>
		<div class="bg-retro-blue h-px flex-1"></div>
		<div class="japanese-text">技術</div>
	</div>

	<div class="space-y-12">
		<!-- Header -->
		<div>
			<h2 class="mb-8 text-5xl font-black tracking-[-0.02em] uppercase lg:text-6xl">
				<span class="retro-blue">SKILLS</span>
			</h2>
		</div>

		<!-- Skills Categories -->
		<div class="space-y-12">
			{#each skills as category}
				<div class="space-y-6">
					<h3 class="retro-blue text-lg font-semibold tracking-wide uppercase">
						{category.category}
					</h3>

					<!-- Skills Grid -->
					<div class="grid grid-cols-1 gap-4 sm:grid-cols-2 lg:grid-cols-3">
						{#each category.skills as skill}
							<div class="border-foreground hover:bg-muted/50 border p-4 transition-colors">
								<div class="text-sm font-medium">{skill.name}</div>
								{#if skill.level}
									<div class="text-muted-foreground mt-1 font-mono text-xs uppercase">
										{skill.level}
									</div>
								{/if}
							</div>
						{/each}
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
