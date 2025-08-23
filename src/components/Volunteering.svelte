<script lang="ts">
	import volunteerData from '../data/volunteer.json';

	let volunteer: any[] = volunteerData;
</script>

<section id="volunteering" class="no-animation relative">
	<!-- Simple Grid Overlay -->
	<div class="pointer-events-none absolute inset-0 opacity-5">
		<div class="grid h-full grid-cols-12 gap-8">
			{#each Array(12) as _, i}
				<div class="border-retro-blue border-r"></div>
			{/each}
		</div>
	</div>

	<div class="relative z-10 mx-auto w-full max-w-5xl px-8 lg:px-16">
		<div class="space-y-16">
			<!-- Header -->
			<div class="space-y-8">
				<!-- Section Number -->
				<div class="flex items-center space-x-6">
					<div class="text-muted-foreground font-mono text-xs tracking-[0.3em] uppercase">006</div>
					<div class="bg-retro-blue h-px flex-1"></div>
				</div>

				<!-- Title with Japanese -->
				<div class="space-y-4">
					<h2 class="text-6xl font-black tracking-[-0.02em] uppercase md:text-7xl">
						<span class="japanese-text">奉仕</span><br />
						VOLUNTEER
					</h2>
					<div class="brutalist-box inline-block">
						<span class="japanese-text">コミュニティ</span> COMMUNITY SERVICE
					</div>
				</div>
			</div>

			<!-- Volunteer Timeline -->
			<div class="space-y-16">
				{#each volunteer as vol, id}
					<div class="grid grid-cols-12 gap-8 lg:gap-16">
						<!-- Timeline & Meta -->
						<div class="col-span-12 lg:col-span-4">
							<div class="space-y-6">
								<!-- Volunteer Number -->
								<div class="flex items-center space-x-4">
									<div class="text-retro-red text-4xl font-black">
										{String(id + 1).padStart(2, '0')}
									</div>
									<div class="bg-retro-red h-px flex-1"></div>
								</div>

								<!-- Meta Information -->
								<div class="space-y-3">
									<div class="border-retro-green border-l-2 pl-4">
										<div class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
											{vol.duration}
										</div>
										{#if vol.type}
											<div class="text-retro-green font-mono text-xs tracking-wide uppercase">
												{vol.type}
											</div>
										{/if}
									</div>
								</div>
							</div>
						</div>

						<!-- Content -->
						<div class="col-span-12 lg:col-span-8">
							<div class="space-y-6">
								<!-- Title & Organization -->
								<div class="space-y-3">
									<h3 class="text-2xl font-bold tracking-wide uppercase">{vol.organization}</h3>
									<h4 class="japanese-text text-lg font-medium">{vol.title}</h4>
									{#if vol.japaneseTitle}
										<div class="text-muted-foreground font-light">
											{vol.japaneseTitle}
										</div>
									{/if}
								</div>

								<!-- Description -->
								{#if vol.description}
									<div class="border-retro-yellow border-l-2 pl-4">
										<p class="text-muted-foreground leading-relaxed font-light">
											{vol.description}
										</p>
									</div>
								{/if}

								<!-- Impact & Philosophy -->
								<div class="grid grid-cols-1 gap-6 lg:grid-cols-2">
									{#if vol.impact}
										<div class="space-y-2">
											<h5 class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
												<span class="japanese-text">影響</span> IMPACT
											</h5>
											<div class="border-retro-blue border-l-2 pl-4">
												<span class="text-sm font-medium">{vol.impact}</span>
											</div>
										</div>
									{/if}

									{#if vol.philosophy}
										<div class="space-y-2">
											<h5 class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
												<span class="japanese-text">哲学</span> PHILOSOPHY
											</h5>
											<div class="border-retro-red border-l-2 pl-4">
												<span class="text-sm font-light italic">{vol.philosophy}</span>
											</div>
										</div>
									{/if}
								</div>
							</div>
						</div>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>
