<script lang="ts">
	import { HardDrive, Zap, Keyboard, FileText, GitBranch } from 'lucide-svelte';

	const differentiators = [
		{
			icon: HardDrive,
			title: 'Local-first = privacy + offline',
			description: 'Your data never leaves your machine. Read, search, and organize without internet.'
		},
		{
			icon: Zap,
			title: 'Rust performance = instant',
			description: 'Sub-100ms operations. No loading spinners, no waiting. Just speed.'
		},
		{
			icon: Keyboard,
			title: 'Keyboard-native = zero friction',
			description: 'Designed for the terminal. Fuzzy finding, completions, and scriptable commands.'
		},
		{
			icon: FileText,
			title: 'Markdown cache = readable anywhere',
			description: 'Articles saved as clean Markdown. Open in any editor, grep through content.'
		},
		{
			icon: GitBranch,
			title: 'Git-syncable SQLite = reliability',
			description: 'Simple database file. Version control your reading list, sync with Git.'
		}
	];
</script>

<section class="bg-bg-primary py-16 md:py-24">
	<div class="mx-auto max-w-(--max-content) px-6">
		<!-- Section header -->
		<div class="mx-auto max-w-(--max-narrow) text-center mb-12">
			<h2 class="heading-section mb-4 text-text-primary">
				Why Stash?
			</h2>
			<p class="body-base text-text-secondary">
				What makes this different from Pocket, Instapaper, or browser bookmarks.
			</p>
		</div>

		<!-- Differentiators grid -->
		<div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each differentiators as item, index}
				<div 
					class="card-accent bg-bg-secondary border border-border rounded p-6 {index >= 3 ? 'lg:col-span-1' : ''}"
					class:lg:last:col-start-2={differentiators.length === 5 && index === 4}
				>
					<div class="flex items-center gap-3 mb-3">
						<item.icon size={20} strokeWidth={1.5} class="text-accent" />
						<h3 class="font-semibold text-text-primary">{item.title}</h3>
					</div>
					<p class="text-sm text-text-secondary leading-relaxed">{item.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
