<script lang="ts">
	const workflows = [
		{
			title: 'Save articles instantly',
			description:
				'Copy a URL from your browser and save it with tags. Stash automatically fetches the title, description, and content.',
			code: `<span class="token-comment"># Save from clipboard</span>
<span class="token-command">$ stash add</span> <span class="token-arg">https://example.com/article</span> <span class="token-flag">#rust #programming</span>

<span class="token-success">✓ Saved: Building Fast CLI Tools in Rust</span>
<span class="text-text-muted">  ID: 15 • example.com • 2 tags</span>`
		},
		{
			title: 'Organize with tags',
			description:
				'Tag your articles for easy organization. Search by tags, filter by site, or use full-text search to find what you need.',
			code: `<span class="token-comment"># List articles by tag</span>
<span class="token-command">$ stash ls</span> <span class="token-flag">--tag rust</span>

<span class="text-text-secondary">15 ★ Building Fast CLI Tools in Rust</span>
<span class="text-text-secondary">12   Async Programming in Rust</span>
<span class="text-text-secondary">8    Rust 1.82.0 Release Notes</span>`
		},
		{
			title: 'Fuzzy finding with pick',
			description:
				'Use the interactive fuzzy finder to quickly browse and open articles. Powered by fzf for lightning-fast searching.',
			code: `<span class="token-comment"># Interactive fuzzy finder</span>
<span class="token-command">$ stash pick</span>

<span class="text-text-secondary">> rust async</span>
<span class="text-text-muted">  15/42 articles</span>

<span class="text-accent">▸ Building Fast CLI Tools in Rust</span>
<span class="text-text-secondary">  Async Programming in Rust</span>
<span class="text-text-secondary">  Rust 1.82.0 Release Notes</span>`
		},
		{
			title: 'Read offline anywhere',
			description:
				'Articles are saved as clean Markdown. Read in your terminal with your favorite pager, or export to any format.',
			code: `<span class="token-comment"># Read in terminal</span>
<span class="token-command">$ stash open</span> <span class="token-arg">15</span> <span class="token-flag">--read</span>

<span class="text-text-primary"># Building Fast CLI Tools in Rust</span>
<span class="text-text-muted">example.com • 5 min read</span>

<span class="text-text-secondary">Command-line tools are everywhere...</span>`
		}
	];
</script>

<section class="bg-bg-secondary py-16 md:py-24">
	<div class="mx-auto max-w-(--max-content) px-6">
		<!-- Section header -->
		<div class="mb-12 text-center">
			<h2 class="heading-section mb-4 text-text-primary">Stash in action</h2>
			<p class="body-base text-text-secondary">See how Stash fits into your workflow</p>
		</div>

		<!-- Workflows -->
		<div class="space-y-16 md:space-y-20">
			{#each workflows as workflow, index}
				<div
					class="grid items-center gap-8 md:grid-cols-2 md:gap-12"
				>
					<!-- Text content -->
					<div class={index % 2 === 1 ? 'md:order-2' : ''}>
						<h3 class="mb-3 text-xl font-semibold text-text-primary">{workflow.title}</h3>
						<p class="text-text-secondary leading-relaxed">{workflow.description}</p>
					</div>

					<!-- Code example -->
					<div class={index % 2 === 1 ? 'md:order-1' : ''}>
						<div class="terminal-window">
							<div class="terminal-header">
								<div class="terminal-dot bg-[#ff5f56]"></div>
								<div class="terminal-dot bg-[#ffbd2e]"></div>
								<div class="terminal-dot bg-[#27ca40]"></div>
							</div>
							<div class="terminal-body">
								{@html workflow.code}
							</div>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

