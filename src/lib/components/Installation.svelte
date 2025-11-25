<script lang="ts">
	import { Copy, Check, Terminal } from 'lucide-svelte';

	let copiedIndex = $state<number | null>(null);

	const installMethods = [
		{
			name: 'Homebrew',
			description: 'Recommended for macOS and Linux',
			command: 'brew install ayushman/stash/stash'
		},
		{
			name: 'Shell script',
			description: 'Direct install for Linux',
			command: 'curl -sSL https://stash.sh/install.sh | sh'
		}
	];

	async function copyToClipboard(command: string, index: number) {
		try {
			await navigator.clipboard.writeText(command);
			copiedIndex = index;
			setTimeout(() => (copiedIndex = null), 2000);
		} catch (err) {
			console.error('Failed to copy:', err);
		}
	}
</script>

<section class="bg-bg-secondary py-16 md:py-24">
	<div class="mx-auto max-w-(--max-content) px-6">
		<div class="mx-auto max-w-(--max-narrow)">
			<!-- Section header -->
			<div class="text-center mb-10">
				<h2 class="heading-section mb-4 text-text-primary">
					Installation
				</h2>
				<p class="body-base text-text-secondary">
					Get started in seconds.
				</p>
			</div>

			<!-- Install options -->
			<div class="space-y-4">
				{#each installMethods as method, index}
					<div class="rounded border border-border bg-bg-primary p-5">
						<div class="flex items-center justify-between mb-3">
							<div>
								<h3 class="font-semibold text-text-primary">{method.name}</h3>
								<p class="text-sm text-text-muted">{method.description}</p>
							</div>
						</div>
						<div class="flex items-center gap-3 rounded bg-bg-tertiary px-4 py-3 font-mono text-sm">
							<Terminal size={16} strokeWidth={1.5} class="text-text-muted shrink-0" />
							<code class="text-text-primary flex-1 overflow-x-auto">{method.command}</code>
							<button
								onclick={() => copyToClipboard(method.command, index)}
								class="shrink-0 text-text-muted hover:text-accent transition-colors"
								aria-label="Copy to clipboard"
							>
								{#if copiedIndex === index}
									<Check size={16} strokeWidth={2} class="text-green-500" />
								{:else}
									<Copy size={16} strokeWidth={2} />
								{/if}
							</button>
						</div>
					</div>
				{/each}
			</div>

			<!-- After install hint -->
			<p class="mt-6 text-center text-sm text-text-muted font-mono">
				After install, run <code class="text-accent">stash --help</code> to get started.
			</p>
		</div>
	</div>
</section>
