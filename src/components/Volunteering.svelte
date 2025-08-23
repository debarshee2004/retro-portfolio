<script lang="ts">
	import volunteerData from '../data/volunteer.json';

	let volunteer: any[] = volunteerData;
</script>

<section id="volunteering" class="no-animation relative">
	<!-- Section Number -->
	<div class="mb-12 flex items-center space-x-6">
		<div class="text-muted-foreground font-mono text-xs tracking-[0.3em] uppercase">005</div>
		<div class="bg-retro-blue h-px flex-1"></div>
		<div class="japanese-text">奉仕</div>
	</div>

	<div class="space-y-12">
		<!-- Header -->
		<div>
			<h2 class="mb-8 text-5xl font-black tracking-[-0.02em] uppercase lg:text-6xl">
				<span class="retro-blue">VOLUNTEER</span>
			</h2>
		</div>

		<!-- Volunteer Timeline -->
		<div class="space-y-12">
			{#each volunteer as vol}
				<div class="grid grid-cols-12 gap-8">
					<!-- Timeline Info -->
					<div class="col-span-12 lg:col-span-3">
						<div class="space-y-2">
							<div class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
								{vol.duration}
							</div>
							{#if vol.location}
								<div class="text-muted-foreground text-sm">{vol.location}</div>
							{/if}
							{#if vol.status}
								<div class="flex items-center space-x-2">
									<div
										class={`h-2 w-2 rounded-full ${vol.status === 'ongoing' ? 'bg-green-500' : 'bg-muted-foreground'}`}
									></div>
									<span class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
										{vol.status}
									</span>
								</div>
							{/if}
						</div>
					</div>

					<!-- Content -->
					<div class="col-span-12 lg:col-span-9">
						<div class="border-retro-blue space-y-4 border-l-2 pl-6">
							<div class="space-y-2">
								<h3 class="text-xl font-semibold">{vol.organization}</h3>
								<h4 class="retro-blue font-medium">{vol.title}</h4>
							</div>

							{#if vol.description}
								<p class="text-muted-foreground leading-relaxed">{vol.description}</p>
							{/if}

							{#if vol.impact}
								<div class="space-y-2">
									<div class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
										Impact
									</div>
									<p class="text-muted-foreground text-sm leading-relaxed">
										{vol.impact}
									</p>
								</div>
							{/if}

							{#if vol.skills && vol.skills.length > 0}
								<div class="space-y-2">
									<div class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
										Skills Used
									</div>
									<div class="flex flex-wrap gap-2">
										{#each vol.skills as skill}
											<span class="border-foreground border px-2 py-1 font-mono text-xs uppercase">
												{skill}
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
