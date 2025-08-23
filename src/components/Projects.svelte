<script lang="ts">
	import projectsData from '../data/projects.json';

	let projects: any[] = projectsData;
</script>

<section id="projects" class="relative">
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
			<div class="no-animation space-y-8">
				<!-- Section Number -->
				<div class="flex items-center space-x-6">
					<div class="text-muted-foreground font-mono text-xs tracking-[0.3em] uppercase">005</div>
					<div class="bg-retro-blue h-px flex-1"></div>
				</div>

				<!-- Title with Japanese -->
				<div class="space-y-4">
					<h2 class="brutal-title">
						<span class="japanese-kanji">作品集</span><br />
						PROJECTS
					</h2>
					<div class="brutalist-box japanese-float">
						<span class="japanese-kanji">創造物</span> CREATIVE WORK
					</div>
				</div>

				<!-- Description -->
				<div class="max-w-2xl">
					<div class="brutalist-card">
						<p class="leading-relaxed font-medium">
							Selected work showcasing expertise in <span class="japanese-kanji">機械学習</span> (machine
							learning), full-stack development, and innovative solutions across various domains.
						</p>
					</div>
				</div>
			</div>

			<!-- Projects Grid -->
			<div class="space-y-20">
				{#each projects as project, id}
					<div class="no-animation grid grid-cols-12 gap-8 lg:gap-16">
						<!-- Project Number & Info -->
						<div class="col-span-12 lg:col-span-4">
							<div class="space-y-6">
								<!-- Project Number with Japanese styling -->
								<div class="flex items-center space-x-4">
									<div class="text-retro-blue text-6xl font-black">
										{String(id + 1).padStart(2, '0')}
									</div>
									<div class="bg-retro-blue h-px flex-1"></div>
								</div>

								<!-- Project Meta -->
								<div class="space-y-4">
									<div class="space-y-3">
										<h3 class="mb-2 text-2xl font-bold tracking-wide uppercase">{project.title}</h3>
										{#if project.japaneseTitle}
											<div class="japanese-text text-lg font-medium">
												{project.japaneseTitle}
											</div>
										{/if}

										<div class="flex flex-wrap gap-2">
											{#if project.status === 'featured'}
												<div class="brutalist-box inline-block">
													<span class="japanese-text">特集</span> FEATURED
												</div>
											{:else}
												<div
													class="border-retro-red bg-background border px-3 py-1 font-mono text-xs tracking-wider uppercase"
												>
													<span class="japanese-text">作品</span>
													{project.status?.toUpperCase() || 'PROJECT'}
												</div>
											{/if}

											{#if project.category}
												<div
													class="border-retro-blue bg-background border px-3 py-1 font-mono text-xs tracking-wider uppercase"
												>
													{project.category}
												</div>
											{/if}

											{#if project.year}
												<div
													class="border-retro-yellow bg-background border px-3 py-1 font-mono text-xs tracking-wider uppercase"
												>
													{project.year}
												</div>
											{/if}
										</div>
									</div>

									<div class="border-retro-yellow border-l-2 pl-4">
										<p class="text-muted-foreground leading-relaxed font-light">
											{project.description}
										</p>
									</div>
								</div>
							</div>
						</div>

						<!-- Project Details -->
						<div class="col-span-12 lg:col-span-8">
							<div class="space-y-8">
								<!-- Project Visual with Japanese aesthetic -->
								<div class="border-foreground relative aspect-video overflow-hidden border-2">
									<div
										class="from-retro-blue/10 to-retro-red/20 absolute inset-0 bg-gradient-to-br"
									></div>
									<div class="absolute inset-0 flex items-center justify-center">
										<div class="space-y-2 text-center">
											<div class="japanese-text text-4xl font-black">
												{project.title.charAt(0)}
											</div>
											<div
												class="text-muted-foreground/50 font-mono text-xs tracking-wider uppercase"
											>
												{project.title.split(' ')[0]}
											</div>
										</div>
									</div>
									<!-- Grid overlay on project visual -->
									<div class="pointer-events-none absolute inset-0 opacity-10">
										<div class="grid h-full grid-cols-8 gap-2">
											{#each Array(8) as _, i}
												<div class="border-retro-blue border-r"></div>
											{/each}
										</div>
									</div>
								</div>

								<!-- Technologies & Links with Japanese styling -->
								<div class="grid grid-cols-1 gap-8 lg:grid-cols-2">
									<!-- Technologies -->
									<div class="space-y-4">
										<h4
											class="border-retro-red border-l-2 pl-4 font-mono text-xs tracking-wider uppercase"
										>
											<span class="japanese-text">技術</span> TECHNOLOGIES
										</h4>
										<div class="space-y-2">
											{#each project.technologies as tech}
												<div class="flex items-center space-x-3">
													<div class="bg-retro-blue h-1 w-1"></div>
													<span class="text-sm font-medium">{tech}</span>
												</div>
											{/each}
										</div>
									</div>

									<!-- Links -->
									<div class="space-y-4">
										<h4
											class="border-retro-yellow border-l-2 pl-4 font-mono text-xs tracking-wider uppercase"
										>
											<span class="japanese-text">リンク</span> LINKS
										</h4>
										<div class="space-y-3">
											{#if project.github}
												<a
													href={project.github}
													target="_blank"
													rel="noopener noreferrer"
													class="hover:text-retro-blue group flex items-center font-mono text-sm tracking-wide uppercase transition-colors"
												>
													<div
														class="bg-retro-blue mr-3 h-px w-2 transition-all group-hover:w-4"
													></div>
													<span>GitHub</span>
												</a>
											{/if}
											{#if project.live}
												<a
													href={project.live}
													target="_blank"
													rel="noopener noreferrer"
													class="hover:text-retro-red group flex items-center font-mono text-sm tracking-wide uppercase transition-colors"
												>
													<div
														class="bg-retro-red mr-3 h-px w-2 transition-all group-hover:w-4"
													></div>
													<span>Live Demo</span>
												</a>
											{/if}
										</div>
									</div>
								</div>
							</div>
						</div>
					</div>
				{/each}
			</div>

			<!-- Checkout my Projects Button -->
			<div class="mt-16 flex justify-center">
				<a
					target="_blank"
					href="https://github.com/debarshee2004"
					class="brutalist-box text-center no-underline"
				>
					<span class="japanese-text">もっと</span> MORE PROJECTS
				</a>
			</div>
		</div>
	</div>
</section>
