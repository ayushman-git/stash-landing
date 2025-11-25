<script lang="ts">
	import { Github, GitPullRequest, Bug, Lightbulb, Heart } from 'lucide-svelte';

	const contributionTypes = [
		{
			icon: Bug,
			title: 'Report bugs',
			description: 'Found something broken? Let me know with steps to reproduce.'
		},
		{
			icon: Lightbulb,
			title: 'Suggest features',
			description: "Got an idea that would make Stash better? I'm all ears."
		},
		{
			icon: GitPullRequest,
			title: 'Submit PRs',
			description: "Want to contribute code? Even more welcome. Let's build this together."
		}
	];
</script>

<section class="bg-bg-primary py-16 md:py-24">
	<div class="mx-auto max-w-(--max-content) px-6">
		<div class="mx-auto max-w-(--max-narrow)">
			<!-- Section header -->
			<div class="text-center mb-12">
				<p class="mb-3 font-mono text-sm text-text-muted">// made with love</p>
				<h2 class="heading-section mb-4 text-text-primary">
					Built solo, open to all
				</h2>
				<p class="body-base text-text-secondary">
					Stash started as a weekend project to scratch my own itch. Now it's out there, free and open source. If it helps you too, that makes me happy.
				</p>
			</div>

			<!-- Contribution types -->
			<div class="grid gap-4 sm:grid-cols-3 mb-10">
				{#each contributionTypes as item (item.title)}
					<div class="rounded border border-border bg-bg-secondary p-5 text-center">
						<div class="mb-3 flex justify-center">
							<item.icon size={24} strokeWidth={1.5} class="text-accent" />
						</div>
						<h3 class="font-semibold text-text-primary mb-2">{item.title}</h3>
						<p class="text-sm text-text-secondary leading-relaxed">{item.description}</p>
					</div>
				{/each}
			</div>

			<!-- CTA -->
			<div class="text-center">
				<a
					href="https://github.com/ayushman-git/stash"
					target="_blank"
					rel="noopener noreferrer"
					class="inline-flex items-center gap-2 rounded bg-terminal-dark px-6 py-3 font-mono text-sm text-terminal-text transition-all hover:opacity-90"
				>
					<Github size={18} strokeWidth={1.5} />
					<span>View on GitHub</span>
				</a>
				<p class="mt-4 text-sm text-text-muted">
					<Heart size={14} strokeWidth={2} class="inline-block mr-1 text-accent" />
					Every star, issue, or PR means a lot.
				</p>
			</div>
		</div>
	</div>
</section>
