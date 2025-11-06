<script lang="ts">
	const features = [
		{
			icon: '🔒',
			title: 'Local-First & Private',
			description:
				'All your data stays on your machine. No cloud, no tracking, no third parties. SQLite database you control.'
		},
		{
			icon: '⚡',
			title: 'Lightning Fast',
			description:
				'Built in Rust for maximum performance. Sub-100ms operations. Start reading instantly, no waiting.'
		},
		{
			icon: '⌨️',
			title: 'Keyboard-Driven',
			description:
				'Designed for power users. Minimal typing, maximum efficiency. Fuzzy finding with fzf integration.'
		},
		{
			icon: '🏷️',
			title: 'Smart Organization',
			description:
				'Tag, search, and filter your articles. Auto-tagging by domain. Full-text search across all content.'
		},
		{
			icon: '📖',
			title: 'Offline Reading',
			description:
				'Articles cached as clean Markdown. Read anywhere, anytime. No internet required after saving.'
		},
		{
			icon: '🔄',
			title: 'Git-Syncable',
			description:
				'Simple SQLite database. Sync across devices using Git. Version control for your reading list.'
		}
	];
</script>

<section class="relative bg-dark-green-950 py-24">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<!-- Section header -->
		<div class="mb-16 text-center">
			<h2 class="mb-4 font-['Inter'] text-4xl font-bold text-white sm:text-5xl">
				Everything you need to manage your reading
			</h2>
			<p class="text-xl text-gray-400">
				Built for developers who value speed, privacy, and control
			</p>
		</div>

		<!-- Features grid -->
		<div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
			{#each features as feature}
				<div
					class="group rounded-xl border border-dark-green-700/30 bg-dark-green-900/30 p-8 backdrop-blur-sm transition-all hover:border-accent-green-500/50 hover:bg-dark-green-800/50"
				>
					<div
						class="mb-4 flex h-14 w-14 items-center justify-center rounded-lg bg-accent-green-500/10 text-3xl transition-transform group-hover:scale-110"
					>
						{feature.icon}
					</div>
					<h3 class="mb-3 text-xl font-semibold text-white">{feature.title}</h3>
					<p class="leading-relaxed text-gray-400">{feature.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

