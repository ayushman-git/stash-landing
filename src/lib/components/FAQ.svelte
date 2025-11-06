<script lang="ts">
	let openIndex = $state<number | null>(null);

	const faqs = [
		{
			question: 'How does Stash differ from Pocket or Instapaper?',
			answer:
				'Stash is a local-first CLI tool that stores everything on your machine. Unlike cloud services, your data never leaves your computer. It\'s built for developers who prefer keyboard-driven workflows and want complete control over their data. Plus, it\'s free and open source.'
		},
		{
			question: 'Where is my data stored?',
			answer:
				'All your articles are stored in a SQLite database on your local machine (typically in ~/.local/share/stash/). The content is saved as clean Markdown for easy access. You can backup, sync via Git, or export your data anytime.'
		},
		{
			question: 'Can I sync across devices?',
			answer:
				'Yes! Since Stash uses a simple SQLite database, you can sync it across devices using Git, Dropbox, iCloud, or any file sync service. You can also export/import your articles as JSON for easy migration.'
		},
		{
			question: 'Is it free and open source?',
			answer:
				'Yes, Stash is completely free and open source. You can view the source code, contribute, or fork it on GitHub. No subscriptions, no premium tiers, no tracking.'
		},
		{
			question: 'Does it work offline?',
			answer:
				'Absolutely! Once you save an article, the full content is cached locally as Markdown. You can read, search, and organize your articles without any internet connection.'
		},
		{
			question: 'What about browser integration?',
			answer:
				'While Stash is primarily a CLI tool, you can easily save articles from your browser by copying the URL and using "stash add --from-clipboard". Browser extensions are planned for future releases.'
		}
	];

	function toggle(index: number) {
		openIndex = openIndex === index ? null : index;
	}
</script>

<section class="relative bg-dark-green-950 py-24">
	<div class="mx-auto max-w-4xl px-6 lg:px-8">
		<!-- Section header -->
		<div class="mb-16 text-center">
			<h2 class="mb-4 font-['Inter'] text-4xl font-bold text-white sm:text-5xl">
				Everything you need to know
			</h2>
			<p class="text-xl text-gray-400">Common questions about Stash</p>
		</div>

		<!-- FAQ items -->
		<div class="space-y-4">
			{#each faqs as faq, index}
				<div
					class="overflow-hidden rounded-xl border border-dark-green-700/30 bg-dark-green-900/30 backdrop-blur-sm transition-all hover:border-accent-green-500/30"
				>
					<button
						onclick={() => toggle(index)}
						class="flex w-full items-center justify-between p-6 text-left transition-colors hover:bg-dark-green-800/30"
					>
						<span class="pr-4 text-lg font-semibold text-white">{faq.question}</span>
						<svg
							class="h-6 w-6 flex-shrink-0 text-accent-green-500 transition-transform {openIndex ===
							index
								? 'rotate-180'
								: ''}"
							fill="none"
							stroke="currentColor"
							viewBox="0 0 24 24"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M19 9l-7 7-7-7"
							></path>
						</svg>
					</button>
					{#if openIndex === index}
						<div class="border-t border-dark-green-700/30 p-6 pt-4">
							<p class="leading-relaxed text-gray-400">{faq.answer}</p>
						</div>
					{/if}
				</div>
			{/each}
		</div>
	</div>
</section>

