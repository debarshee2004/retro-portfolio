<script lang="ts">
	const currentYear = new Date().getFullYear();

	// Fun interactive state
	let clickCount = 0;
	let showSecret = false;
	let konamiCode = [];
	let funMessages = [
		'Hello there! 👋',
		'You found me! 🎉',
		'Keep clicking! 🚀',
		'Almost there... 🎯',
		"SURPRISE! 🎊 You're awesome!",
		'頑張って！ (Keep going!) 💪',
		'Achievement unlocked! 🏆',
		"You're persistent! 🔥"
	];

	let currentMessage = '';
	let showEasterEgg = false;

	// Fun click handler
	function handleTitleClick() {
		clickCount++;
		currentMessage = funMessages[Math.min(clickCount - 1, funMessages.length - 1)];

		if (clickCount >= 5) {
			showEasterEgg = true;
		}

		// Reset after showing all messages
		if (clickCount > funMessages.length + 2) {
			clickCount = 0;
			showEasterEgg = false;
			currentMessage = '';
		}
	}

	// Random emoji generator
	function getRandomEmoji() {
		const emojis = ['🎌', '🗾', '🍜', '🍱', '🎋', '⛩️', '🌸', '🍙', '🍘', '🗻'];
		return emojis[Math.floor(Math.random() * emojis.length)];
	}

	// Time-based greeting
	function getTimeBasedGreeting() {
		const hour = new Date().getHours();
		if (hour < 12) return { jp: 'おはよう', en: 'GOOD MORNING' };
		if (hour < 18) return { jp: 'こんにちは', en: 'GOOD AFTERNOON' };
		return { jp: 'こんばんは', en: 'GOOD EVENING' };
	}

	let greeting = getTimeBasedGreeting();
</script>

<footer class="border-foreground/20 relative mt-24 border-t pt-16">
	<!-- Simple Grid Overlay -->
	<div class="pointer-events-none absolute inset-0 opacity-5">
		<div class="grid h-full grid-cols-12 gap-8">
			{#each Array(12) as _, i}
				<div class="border-japanese-blue border-r"></div>
			{/each}
		</div>
	</div>

	<div class="relative z-10 mx-auto w-full max-w-[1600px] px-8 lg:px-16">
		<div class="space-y-16">
			<!-- Header -->
			<div class="space-y-8">
				<!-- Title with Japanese -->
				<div class="space-y-4">
					<button
						class="brutal-title cursor-pointer border-none bg-transparent p-0 text-4xl transition-transform hover:scale-105 md:text-6xl"
						on:click={handleTitleClick}
						title="Click me for a surprise!"
					>
						<span class="japanese-kanji">終了</span> FOOTER
					</button>
					<div class="brutalist-box japanese-float">
						<span class="japanese-kanji">さようなら</span> SAYONARA
					</div>

					<!-- Interactive message display -->
					{#if currentMessage}
						<div class="brutalist-card japanese-gold-bg animate-bounce text-black">
							<p class="text-center text-sm font-bold">{currentMessage}</p>
						</div>
					{/if}
				</div>

				<!-- Quirky Fun Elements -->
				<div class="mt-8 grid grid-cols-1 gap-4 md:grid-cols-3">
					<!-- Fun Fact 1 -->
					<div class="brutalist-card-blue text-center transition-transform hover:rotate-3">
						<div class="japanese-kanji mb-2 animate-pulse text-2xl">🚀</div>
						<p class="text-xs font-bold">
							POWERED BY<br /><span class="japanese-kanji">情熱</span> PASSION
						</p>
						<div class="mt-2 text-xs opacity-75">
							Level: {clickCount > 0 ? 'ACTIVATED' : 'DORMANT'}
						</div>
					</div>

					<!-- Fun Fact 2 -->
					<div
						class="brutalist-card japanese-gold-bg text-center text-black transition-transform hover:-rotate-2"
					>
						<div class="mb-2 animate-bounce text-2xl">⚡</div>
						<p class="text-xs font-bold">
							MADE WITH<br /><span class="japanese-kanji">愛</span> LOVE & COFFEE
						</p>
						<div class="mt-2 text-xs opacity-75">{greeting.jp} {getRandomEmoji()}</div>
					</div>

					<!-- Fun Fact 3 -->
					<div
						class="brutalist-card japanese-red-bg text-center text-white transition-transform hover:rotate-1"
					>
						<div class="japanese-kanji mb-2 text-2xl">🎯</div>
						<p class="text-xs font-bold">
							BUILDING<br /><span class="japanese-kanji">未来</span> THE FUTURE
						</p>
						<div class="mt-2 text-xs opacity-75">Status: {greeting.en}</div>
					</div>
				</div>

				<!-- Easter Egg Section -->
				{#if showEasterEgg}
					<div class="brutalist-card japanese-blue-bg animate-pulse text-center text-white">
						<div class="mb-4 text-4xl">🎊 🎉 🎊</div>
						<h3 class="brutal-subtitle mb-2 text-white">CONGRATULATIONS!</h3>
						<p class="text-sm">You discovered the secret footer feature!</p>
						<p class="japanese-kanji mt-2 text-xs">隠された機能を見つけました！</p>
						<div class="mt-4 flex justify-center space-x-2">
							<span class="animate-spin text-2xl">⭐</span>
							<span class="animate-bounce text-2xl">🏆</span>
							<span class="animate-pulse text-2xl">🎌</span>
						</div>
					</div>
				{/if}

				<!-- ASCII Art Section -->
				<div
					class="brutalist-card japanese-black-bg text-japanese-gold hidden text-center transition-transform hover:scale-105 md:block"
				>
					<pre class="font-mono text-xs leading-tight">
						THANK YOU FOR VISITING!
						また会いましょう
						(See you again!)
      
    					Fun Fact: This site has {clickCount > 0 ? clickCount : 'hidden'} easter eggs! 🥚
					</pre>
				</div>

				<!-- Interactive Stats -->
				<div class="mt-6 grid grid-cols-2 gap-4 md:grid-cols-4">
					<div class="brutalist-card text-center">
						<div class="text-lg font-bold">{currentYear - 2023}+</div>
						<div class="japanese-kanji text-xs">年間経験</div>
						<div class="text-xs">YEARS EXP</div>
					</div>
					<div class="brutalist-card text-center">
						<div class="text-lg font-bold">∞</div>
						<div class="japanese-kanji text-xs">コーヒー</div>
						<div class="text-xs">COFFEES</div>
					</div>
					<div class="brutalist-card text-center">
						<div class="text-lg font-bold">100%</div>
						<div class="japanese-kanji text-xs">情熱</div>
						<div class="text-xs">PASSION</div>
					</div>
					<div class="brutalist-card text-center">
						<div class="text-lg font-bold">{clickCount}</div>
						<div class="japanese-kanji text-xs">クリック</div>
						<div class="text-xs">CLICKS</div>
					</div>
				</div>
			</div>

			<!-- Footer Content -->
			<div class="grid grid-cols-1 gap-8 lg:grid-cols-2 lg:gap-12">
				<!-- Main Message -->
				<div class="brutal-section">
					<h3 class="brutal-subtitle mb-4 text-base md:text-lg">
						Let's Build Something Amazing Together
					</h3>
					<p class="text-sm leading-relaxed font-medium md:text-base">
						I'm always interested in new opportunities and exciting projects. Let's connect and
						create something <span class="japanese-kanji">素晴らしい</span>.
					</p>
				</div>

				<!-- Contact & Links -->
				<div class="grid grid-cols-1 gap-6 sm:grid-cols-2">
					<!-- Quick Links -->
					<div class="brutalist-card transition-transform hover:rotate-1">
						<h4 class="brutal-subtitle mb-4 text-sm">
							<span class="japanese-kanji">リンク</span> LINKS
						</h4>
						<div class="space-y-3">
							<a
								target="_blank"
								href="https://github.com/debarshee2004"
								class="brutalist-button block w-full text-center text-xs transition-transform hover:scale-105"
							>
								GitHub
							</a>
							<a
								data-sveltekit-preload-data="hover"
								href="https://www.dinocodes.in/blogs"
								class="brutalist-button japanese-blue-bg block w-full text-center text-xs text-white transition-transform hover:scale-105"
							>
								Blogs
							</a>
							<a
								data-sveltekit-preload-data="hover"
								href="https://www.dinocodes.in/links"
								class="brutalist-button japanese-gold-bg block w-full text-center text-xs text-black transition-transform hover:scale-105"
							>
								Links
							</a>
						</div>

						<!-- Fun interaction counter -->
						<div class="mt-4 text-center">
							<div class="text-xs opacity-75">
								Visitors today: <span class="font-bold">{Math.floor(Math.random() * 100) + 50}</span
								> 👥
							</div>
						</div>
					</div>

					<!-- Tech Stack -->
					<div
						class="brutalist-card japanese-red-bg text-white transition-transform hover:-rotate-1"
					>
						<h4 class="brutal-subtitle mb-4 text-sm text-white">
							<span class="japanese-kanji">技術</span> BUILT WITH
						</h4>
						<div class="space-y-2 text-xs font-bold">
							<div class="flex items-center justify-between transition-transform hover:scale-110">
								<span>SvelteKit</span>
							</div>
							<div class="flex items-center justify-between transition-transform hover:scale-110">
								<span>Tailwind CSS</span>
							</div>
							<div class="flex items-center justify-between transition-transform hover:scale-110">
								<span>TypeScript</span>
							</div>
							<div class="flex items-center justify-between transition-transform hover:scale-110">
								<span>Cloudflare</span>
							</div>
						</div>

						<!-- Random tech fact -->
						<div class="mt-4 border-t border-white/20 pt-3 text-center">
							<div class="text-xs opacity-90">
								Powered by {Math.floor(Math.random() * 42) + 1} cups of coffee
							</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Bottom Section -->
			<div class="japanese-border mt-12 p-4 md:p-6">
				<div
					class="flex flex-col items-center space-y-4 md:flex-row md:justify-between md:space-y-0"
				>
					<div class="brutal-subtitle text-center text-xs md:text-left md:text-sm">
						© {currentYear} Debarshee Chakraborty. All rights reserved.
					</div>
					<div class="brutal-subtitle text-center text-xs md:text-right md:text-sm">
						<span class="japanese-kanji">作成者</span> CRAFTED WITH LOVE ❤️
					</div>
				</div>

				<!-- Mobile ASCII Art -->
				<div class="brutalist-card japanese-black-bg text-japanese-gold mt-4 text-center md:hidden">
					<div class="text-sm">
						<span class="text-xl">🙏</span> <span class="japanese-kanji">ありがとう</span>
						<span class="text-xl">🙏</span><br />
						<span class="text-xs">THANK YOU!</span>
					</div>
				</div>

				<!-- Fun footer signature -->
				<div class="mt-6 text-center">
					<div class="brutalist-card japanese-blue-bg inline-block text-white">
						<div class="text-xs">
							Made with <span class="animate-pulse">�</span> in
							<span class="japanese-kanji">日本風</span>
							style
							{#if clickCount > 3}
								<br />🎉 You're a curious explorer! 🎉
							{/if}
						</div>
					</div>
				</div>

				<!-- Secret message for persistent clickers -->
				{#if clickCount > 7}
					<div class="mt-4 text-center">
						<div class="brutalist-card japanese-gold-bg animate-bounce text-black">
							<div class="text-sm font-bold">
								🏆 MASTER CLICKER ACHIEVEMENT UNLOCKED! 🏆<br />
								<span class="japanese-kanji text-xs">クリックマスター認定！</span>
							</div>
						</div>
					</div>
				{/if}
			</div>
		</div>
	</div>
</footer>
