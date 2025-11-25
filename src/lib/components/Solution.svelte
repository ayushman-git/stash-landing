<script lang="ts">
	import { Database, Zap, Terminal, HardDrive } from 'lucide-svelte';

	const highlights = [
		{ icon: HardDrive, label: 'Local-first' },
		{ icon: Database, label: 'SQLite-based' },
		{ icon: Zap, label: 'Sub-100ms' },
		{ icon: Terminal, label: 'Unix-style' }
	];
</script>

<section class="bg-bg-secondary py-16 md:py-24">
	<div class="mx-auto max-w-(--max-content) px-6">
		<div class="mx-auto max-w-(--max-narrow)">
			<!-- Section header -->
			<h2 class="heading-section mb-6 text-center text-text-primary">
				The solution
			</h2>

			<!-- Description -->
			<p class="body-large text-center text-text-secondary mb-10">
				Stash is a blazing-fast CLI tool built in Rust for saving and organizing articles. 
				It stores everything locally in a SQLite database, giving you complete control over your data. 
				No accounts, no cloud sync, no tracking. Just predictable Unix-style commands that work offline.
			</p>

			<!-- Highlight badges -->
			<div class="flex flex-wrap justify-center gap-3">
				{#each highlights as item}
					<div class="flex items-center gap-2 rounded border border-border bg-bg-primary px-4 py-2 text-sm">
						<item.icon size={16} strokeWidth={1.5} class="text-accent" />
						<span class="text-text-secondary">{item.label}</span>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>
