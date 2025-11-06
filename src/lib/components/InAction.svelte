<script lang="ts">
	const workflows = [
		{
			title: 'Save articles instantly',
			description:
				'Copy a URL from your browser and save it with tags. Stash automatically fetches the title, description, and content.',
			code: `<span class="token-comment"># Save from clipboard</span>
<span class="token-command">$ stash add</span> <span class="token-arg">https://example.com/article</span> <span class="token-flag">#rust #programming</span>

<span class="text-gray-400">✓ Saved: Building Fast CLI Tools in Rust</span>
<span class="text-gray-500">  ID: 15 • example.com • 2 tags</span>`
		},
		{
			title: 'Organize with tags',
			description:
				'Tag your articles for easy organization. Search by tags, filter by site, or use full-text search to find what you need.',
			code: `<span class="token-comment"># List articles by tag</span>
<span class="token-command">$ stash ls</span> <span class="token-flag">--tag rust</span>

<span class="text-gray-400">15 ★ Building Fast CLI Tools in Rust</span>
<span class="text-gray-400">12   Async Programming in Rust</span>
<span class="text-gray-400">8    Rust 1.82.0 Release Notes</span>`
		},
		{
			title: 'Fuzzy finding with pick',
			description:
				'Use the interactive fuzzy finder to quickly browse and open articles. Powered by fzf for lightning-fast searching.',
			code: `<span class="token-comment"># Interactive fuzzy finder</span>
<span class="token-command">$ stash pick</span>

<span class="text-gray-400">> rust async</span>
<span class="text-gray-500">  15/42 articles</span>

<span class="text-accent-green-400">▸ Building Fast CLI Tools in Rust</span>
<span class="text-gray-400">  Async Programming in Rust</span>
<span class="text-gray-400">  Rust 1.82.0 Release Notes</span>`
		},
		{
			title: 'Read offline anywhere',
			description:
				'Articles are saved as clean Markdown. Read in your terminal with your favorite pager, or export to any format.',
			code: `<span class="token-comment"># Read in terminal</span>
<span class="token-command">$ stash open</span> <span class="token-arg">15</span> <span class="token-flag">--read</span>

<span class="text-gray-400"># Building Fast CLI Tools in Rust</span>
<span class="text-gray-500">example.com • 5 min read</span>

<span class="text-gray-400">Command-line tools are everywhere...</span>`
		}
	];
</script>

<section class="relative bg-dark-green-900/30 py-24">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<!-- Section header -->
		<div class="mb-16 text-center">
			<h2 class="mb-4 font-['Inter'] text-4xl font-bold text-white sm:text-5xl">Stash in action</h2>
			<p class="text-xl text-gray-400">See how Stash fits into your workflow</p>
		</div>

		<!-- Workflows -->
		<div class="space-y-24">
			{#each workflows as workflow, index}
				<div
					class="grid items-center gap-12 lg:grid-cols-2 {index % 2 === 1 ? 'lg:flex-row-reverse' : ''}"
				>
					<!-- Text content -->
					<div class={index % 2 === 1 ? 'lg:order-2' : ''}>
						<h3 class="mb-4 text-3xl font-bold text-white">{workflow.title}</h3>
						<p class="text-lg leading-relaxed text-gray-400">{workflow.description}</p>
					</div>

					<!-- Code example -->
					<div class={index % 2 === 1 ? 'lg:order-1' : ''}>
						<div class="terminal-window">
							<div class="terminal-header">
								<div class="terminal-dot bg-red-500"></div>
								<div class="terminal-dot bg-yellow-500"></div>
								<div class="terminal-dot bg-green-500"></div>
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

