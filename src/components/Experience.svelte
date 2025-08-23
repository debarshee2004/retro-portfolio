<script lang="ts">
	import experienceData from '../data/experience.json';

	let experiences: any[] = experienceData;
</script>

<section id="experience" class="no-animation relative">
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
					<div class="text-muted-foreground font-mono text-xs tracking-[0.3em] uppercase">003</div>
					<div class="bg-retro-blue h-px flex-1"></div>
				</div>

				<!-- Title with Japanese -->
				<div class="space-y-4">
					<h2 class="text-6xl font-black tracking-[-0.02em] uppercase md:text-7xl">
						<span class="japanese-text">経験</span><br />
						EXPERIENCE
					</h2>
					<div class="brutalist-box inline-block">
						<span class="japanese-text">キャリア</span> CAREER PATH
					</div>
				</div>
			</div>

			<!-- Experience Timeline -->
			<div class="space-y-16">
				{#each experiences as work, id}
					<div class="grid grid-cols-12 gap-8 lg:gap-16">
						<!-- Timeline & Meta -->
						<div class="col-span-12 lg:col-span-4">
							<div class="space-y-6">
								<!-- Experience Number -->
								<div class="flex items-center space-x-4">
									<div class="text-retro-blue text-4xl font-black">
										{String(id + 1).padStart(2, '0')}
									</div>
									<div class="bg-retro-blue h-px flex-1"></div>
								</div>

								<!-- Meta Information -->
								<div class="space-y-3">
									<div class="border-retro-yellow border-l-2 pl-4">
										<div class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
											{work.duration}
										</div>
										<div class="text-muted-foreground text-sm">{work.location}</div>
										{#if work.type}
											<div class="text-retro-blue font-mono text-xs tracking-wide uppercase">
												{work.type}
											</div>
										{/if}
									</div>
								</div>
							</div>
						</div>

						<!-- Content -->
						<div class="col-span-12 lg:col-span-8">
							<div class="space-y-6">
								<!-- Title & Company -->
								<div class="space-y-3">
									<h3 class="text-2xl font-bold tracking-wide uppercase">{work.company}</h3>
									<h4 class="japanese-text text-lg font-medium">{work.title}</h4>
									{#if work.japaneseTitle}
										<div class="text-muted-foreground font-light">
											{work.japaneseTitle}
										</div>
									{/if}
								</div>

								<!-- Description -->
								{#if work.description}
									<div class="border-retro-red border-l-2 pl-4">
										<p class="text-muted-foreground leading-relaxed font-light">
											{work.description}
										</p>
									</div>
								{/if}

								<!-- Achievements -->
								{#if work.achievements && work.achievements.length > 0}
									<div class="space-y-3">
										<h5 class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
											<span class="japanese-text">成果</span> ACHIEVEMENTS
										</h5>
										<div class="space-y-2">
											{#each work.achievements as achievement}
												<div class="flex items-start space-x-3">
													<div class="bg-retro-green mt-2 h-1 w-1 flex-shrink-0"></div>
													<span class="text-sm leading-relaxed">{achievement}</span>
												</div>
											{/each}
										</div>
									</div>
								{/if}

								<!-- Technologies -->
								{#if work.technologies && work.technologies.length > 0}
									<div class="space-y-3">
										<h5 class="text-muted-foreground font-mono text-xs tracking-wider uppercase">
											<span class="japanese-text">技術スタック</span> TECH STACK
										</h5>
										<div class="flex flex-wrap gap-2">
											{#each work.technologies as tech}
												<span
													class="border-foreground hover:border-retro-blue border px-3 py-1 font-mono text-xs tracking-wide uppercase transition-colors"
												>
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
	</div>
</section>
