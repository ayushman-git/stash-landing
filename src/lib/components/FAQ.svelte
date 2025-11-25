<script lang="ts">
	import { ChevronDown } from 'lucide-svelte';

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

<section class="bg-bg-primary py-16 md:py-24">
	<div class="mx-auto max-w-(--max-narrow) px-6">
		<!-- Section header -->
		<div class="mb-12 text-center">
			<h2 class="heading-section mb-4 text-text-primary">
				Frequently asked questions
			</h2>
			<p class="body-base text-text-secondary">Common questions about Stash</p>
		</div>

		<!-- FAQ items -->
		<div class="space-y-3">
			{#each faqs as faq, index}
				<div
					class="rounded border border-border bg-bg-secondary transition-colors hover:border-border-light"
				>
					<button
						onclick={() => toggle(index)}
						class="flex w-full items-center justify-between p-5 text-left"
					>
						<span class="pr-4 text-base font-semibold text-text-primary">{faq.question}</span>
						<ChevronDown 
							size={20} 
							strokeWidth={1.5} 
							class="shrink-0 text-text-muted transition-transform {openIndex === index ? 'rotate-180' : ''}" 
						/>
					</button>
					{#if openIndex === index}
						<div class="border-t border-border px-5 pb-5 pt-4">
							<p class="text-sm leading-relaxed text-text-secondary">{faq.answer}</p>
						</div>
					{/if}
				</div>
			{/each}
		</div>
	</div>
</section>

