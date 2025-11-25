<script lang="ts">
	import { Lock, Zap, Keyboard, Tags, BookOpen, RefreshCw } from 'lucide-svelte';

	const features = [
		{
			icon: Lock,
			title: 'Local-First & Private',
			description:
				'All your data stays on your machine. No cloud, no tracking, no third parties. SQLite database you control.'
		},
		{
			icon: Zap,
			title: 'Lightning Fast',
			description:
				'Built in Rust for maximum performance. Sub-100ms operations. Start reading instantly, no waiting.'
		},
		{
			icon: Keyboard,
			title: 'Keyboard-Driven',
			description:
				'Designed for power users. Minimal typing, maximum efficiency. Fuzzy finding with fzf integration.'
		},
		{
			icon: Tags,
			title: 'Smart Organization',
			description:
				'Tag, search, and filter your articles. Auto-tagging by domain. Full-text search across all content.'
		},
		{
			icon: BookOpen,
			title: 'Offline Reading',
			description:
				'Articles cached as clean Markdown. Read anywhere, anytime. No internet required after saving.'
		},
		{
			icon: RefreshCw,
			title: 'Git-Syncable',
			description:
				'Simple SQLite database. Sync across devices using Git. Version control for your reading list.'
		}
	];
</script>

<section class="bg-bg-primary py-16 md:py-24">
	<div class="mx-auto max-w-(--max-content) px-6">
		<!-- Section header -->
		<div class="mb-12 text-center">
			<h2 class="heading-section mb-4 text-text-primary">
				Everything you need
			</h2>
			<p class="body-base text-text-secondary">
				Built for developers who value speed, privacy, and control
			</p>
		</div>

		<!-- Features grid -->
		<div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
			{#each features as feature}
				<div class="card-accent rounded border border-border bg-bg-secondary p-6 transition-colors hover:border-border-light">
					<div class="mb-4 flex h-10 w-10 items-center justify-center rounded bg-accent/10">
						<feature.icon size={20} strokeWidth={1.5} class="text-accent" />
					</div>
					<h3 class="mb-2 font-semibold text-text-primary">{feature.title}</h3>
					<p class="text-sm text-text-secondary leading-relaxed">{feature.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

