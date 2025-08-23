<script lang="ts">
	import experienceData from '../data/experience.json';
	import { onMount } from 'svelte';

	let experiences: any[] = experienceData;
	let mounted = false;

	onMount(() => {
		mounted = true;
	});
</script>

<section id="experience" class="no-animation relative">
	<!-- Section Number -->
	<div class="mb-12 flex items-center space-x-6">
		<div class="text-muted-foreground font-mono text-xs tracking-[0.3em] uppercase">003</div>
		<div class="bg-retro-blue h-px flex-1"></div>
		<div class="japanese-text">経験</div>
	</div>

	<div class="space-y-12">
		<!-- Header -->
		<div>
			<h2 class="mb-8 text-5xl font-black tracking-[-0.02em] uppercase lg:text-6xl">
				<span class="retro-blue">EXPERIENCE</span>
			</h2>
		</div>

		<!-- Experience Timeline -->
		<div class="space-y-12">
			{#each experiences as work, id}
				<div class="grid grid-cols-12 gap-8">
					<!-- Timeline -->
					<div class="col-span-12 lg:col-span-3">
						<div class="space-y-2">
							<div class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
								{work.duration}
							</div>
							<div class="text-muted-foreground text-sm">{work.location}</div>
						</div>
					</div>

					<!-- Content -->
					<div class="col-span-12 lg:col-span-9">
						<div class="border-retro-blue space-y-4 border-l-2 pl-6">
							<div class="space-y-2">
								<h3 class="text-xl font-semibold">{work.company}</h3>
								<h4 class="retro-blue font-medium">{work.title}</h4>
							</div>

							{#if work.description}
								<p class="text-muted-foreground leading-relaxed">{work.description}</p>
							{/if}

							<!-- Technologies -->
							{#if work.technologies && work.technologies.length > 0}
								<div class="space-y-2">
									<div class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
										Tech Stack
									</div>
									<div class="flex flex-wrap gap-2">
										{#each work.technologies as tech}
											<span class="border-foreground border px-2 py-1 font-mono text-xs uppercase">
												{tech}
											</span>
										{/each}
									</div>
								</div>
							{/if}
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
