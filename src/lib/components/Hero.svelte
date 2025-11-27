<script lang="ts">
	import { Check, Copy } from 'lucide-svelte';
	import { Timer, WifiOff, Shield } from 'lucide-svelte';
	import catImage from '$lib/assets/cat.png';

	let copied = $state(false);
	const installCommand = 'brew install ayushman-git/tap/stash';

	async function copyToClipboard() {
		try {
			await navigator.clipboard.writeText(installCommand);
			copied = true;
			setTimeout(() => (copied = false), 2000);
		} catch (err) {
			console.error('Failed to copy:', err);
		}
	}
</script>

<section class="relative min-h-screen bg-bg-primary">
	<!-- Content -->
	<div class="mx-auto max-w-(--max-content) px-6 py-24 lg:py-32">
		<div class="mx-auto max-w-(--max-narrow) text-center">
			<!-- Badge -->
			<div class="mb-8 inline-flex items-center gap-2 rounded border border-border px-3 py-1.5 text-sm text-text-secondary font-mono">
				Built in Rust • Local-First • Open Source
			</div>

			<!-- Headline -->
			<h1 class="heading-display mb-6 text-text-primary">
				Take control of your reading
			</h1>

			<!-- Subheadline -->
			<p class="body-large mb-10 text-text-secondary">
				Fast, local-first CLI tool for saving, organizing, and reading articles.
			</p>

			<!-- Install command -->
			<div class="mb-12 flex justify-center">
				<button
					onclick={copyToClipboard}
					class="group flex items-center gap-3 rounded border border-border bg-bg-secondary px-5 py-3 font-mono text-sm transition-colors hover:border-accent hover:bg-bg-tertiary"
				>
					<span class="text-text-muted">$</span>
					<code class="text-text-primary">{installCommand}</code>
					<span class="text-text-muted transition-colors group-hover:text-accent">
						{#if copied}
							<Check size={16} strokeWidth={2} />
						{:else}
							<Copy size={16} strokeWidth={2} />
						{/if}
					</span>
				</button>
			</div>

			<!-- Terminal preview -->
			<div class="mx-auto max-w-3xl relative">
				<!-- Cat with thought bubble -->
				<div class="absolute -top-[50px] left-2 z-10 group">
					<img
						src={catImage}
						alt="Cat"
						class="w-24 object-contain cursor-pointer"
					/>
					<!-- Thought bubble -->
					<div class="absolute -top-16 left-1/2 -translate-x-1/2 opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none">
						<div class="bg-white text-gray-800 px-3 py-2 rounded-xl text-sm font-medium whitespace-nowrap shadow-lg">
							stash it for later!
						</div>
						<!-- Bubble tail dots -->
						<div class="absolute -bottom-2 left-1/2 -translate-x-1/2 w-3 h-3 bg-white rounded-full"></div>
						<div class="absolute -bottom-4 left-[calc(50%+4px)] w-2 h-2 bg-white rounded-full"></div>
					</div>
				</div>
				<div class="terminal-window">
					<div class="terminal-header">
						<div class="terminal-dot bg-terminal-dot-red"></div>
						<div class="terminal-dot bg-terminal-dot-yellow"></div>
						<div class="terminal-dot bg-terminal-dot-green"></div>
					</div>
					<div class="terminal-body text-left">
						<div class="mb-1">
							<span class="token-comment"># Save an article</span>
						</div>
						<div class="mb-3">
							<span class="token-command">$ stash add</span>
							<span class="token-arg"> https://blog.rust-lang.org/2024/10/17/Rust-1.82.0.html</span>
							<span class="token-flag"> #rust</span>
						</div>
						<div class="mb-1 token-success">✓ Saved: Announcing Rust 1.82.0</div>
						<div class="mb-4 text-text-muted">  ID: 42 • blog.rust-lang.org</div>

						<div class="mb-1">
							<span class="token-comment"># List your articles</span>
						</div>
						<div class="mb-3">
							<span class="token-command">$ stash ls</span>
						</div>
						<div class="text-text-secondary">
							<div class="mb-0.5">42 ★ Announcing Rust 1.82.0 • rust-lang.org • 2m ago</div>
							<div class="mb-0.5">41   Building CLI Tools in Rust • github.com • 1h ago</div>
							<div>40   The Art of Command Line • github.com • 3h ago</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Quick stats -->
			<div class="mt-12 flex flex-wrap items-center justify-center gap-6 text-sm text-text-muted">
				<div class="flex items-center gap-2">
					<Timer size={18} strokeWidth={1.5} class="text-text-muted" />
					<span>Sub-100ms operations</span>
				</div>
				<div class="flex items-center gap-2">
					<WifiOff size={18} strokeWidth={1.5} class="text-text-muted" />
					<span>Offline-first</span>
				</div>
				<div class="flex items-center gap-2">
					<Shield size={18} strokeWidth={1.5} class="text-text-muted" />
					<span>Privacy-focused</span>
				</div>
			</div>
		</div>
	</div>
</section>

