<script lang="ts">
	import InstallButtons from './InstallButtons.svelte';
</script>

<section class="relative min-h-screen overflow-hidden bg-dark-green-950">
	<!-- Geometric background patterns -->
	<div class="absolute inset-0 bg-geometric"></div>
	
	<!-- Decorative circles -->
	<div
		class="absolute right-0 top-0 h-[600px] w-[600px] rounded-full border border-dark-green-700/20"
		style="transform: translate(30%, -30%)"
	></div>
	<div
		class="absolute left-0 top-1/2 h-[400px] w-[400px] rounded-full border border-dark-green-700/20"
		style="transform: translate(-50%, -50%)"
	></div>

	<!-- Grid overlay -->
	<div
		class="absolute inset-0 opacity-10"
		style="background-image: linear-gradient(rgba(77, 222, 128, 0.1) 1px, transparent 1px), linear-gradient(90deg, rgba(77, 222, 128, 0.1) 1px, transparent 1px); background-size: 50px 50px;"
	></div>

	<!-- Content -->
	<div class="relative mx-auto max-w-7xl px-6 py-32 lg:px-8">
		<div class="mx-auto max-w-4xl text-center">
			<!-- Badge -->
			<div class="mb-8 inline-flex items-center gap-2 rounded-full border border-accent-green-500/30 bg-accent-green-500/10 px-4 py-2 text-sm text-accent-green-400">
				<span class="relative flex h-2 w-2">
					<span class="absolute inline-flex h-full w-full animate-ping rounded-full bg-accent-green-400 opacity-75"></span>
					<span class="relative inline-flex h-2 w-2 rounded-full bg-accent-green-500"></span>
				</span>
				Built in Rust • Local-First • Open Source
			</div>

			<!-- Headline -->
			<h1
				class="mb-6 font-['Inter'] text-6xl font-bold leading-tight text-white sm:text-7xl lg:text-8xl"
			>
				Take control of your
				<span
					class="bg-gradient-to-r from-accent-green-400 to-accent-green-600 bg-clip-text text-transparent"
				>
					reading
				</span>
			</h1>

			<!-- Subheadline -->
			<p class="mb-12 text-xl leading-relaxed text-gray-300 sm:text-2xl">
				Fast, local-first CLI tool for saving, organizing, and reading articles.<br />
				Your articles, your way. No cloud, no tracking, just pure speed.
			</p>

			<!-- Install buttons -->
			<div class="mb-16">
				<InstallButtons />
			</div>

			<!-- Terminal preview -->
			<div class="animate-float mx-auto max-w-3xl">
				<div class="terminal-window">
					<div class="terminal-header">
						<div class="terminal-dot bg-red-500"></div>
						<div class="terminal-dot bg-yellow-500"></div>
						<div class="terminal-dot bg-green-500"></div>
					</div>
					<div class="terminal-body">
						<div class="mb-2">
							<span class="token-comment"># Save an article</span>
						</div>
						<div class="mb-4">
							<span class="token-command">$ stash add</span>
							<span class="token-arg"> https://blog.rust-lang.org/2024/10/17/Rust-1.82.0.html</span>
							<span class="token-flag"> #rust</span>
						</div>
						<div class="mb-2 text-gray-400">✓ Saved: Announcing Rust 1.82.0</div>
						<div class="mb-4 text-gray-500">  ID: 42 • blog.rust-lang.org</div>

						<div class="mb-2 mt-6">
							<span class="token-comment"># List your articles</span>
						</div>
						<div class="mb-4">
							<span class="token-command">$ stash ls</span>
						</div>
						<div class="text-gray-400">
							<div class="mb-1">42 ★ Announcing Rust 1.82.0 • rust-lang.org • 2m ago</div>
							<div class="mb-1">41   Building CLI Tools in Rust • github.com • 1h ago</div>
							<div>40   The Art of Command Line • github.com • 3h ago</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Stats or quick info -->
			<div class="mt-16 flex flex-wrap items-center justify-center gap-8 text-sm text-gray-400">
				<div class="flex items-center gap-2">
					<svg class="h-5 w-5 text-accent-green-500" fill="currentColor" viewBox="0 0 20 20">
						<path
							fill-rule="evenodd"
							d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
							clip-rule="evenodd"
						></path>
					</svg>
					<span>Sub-100ms operations</span>
				</div>
				<div class="flex items-center gap-2">
					<svg class="h-5 w-5 text-accent-green-500" fill="currentColor" viewBox="0 0 20 20">
						<path
							fill-rule="evenodd"
							d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
							clip-rule="evenodd"
						></path>
					</svg>
					<span>Offline-first</span>
				</div>
				<div class="flex items-center gap-2">
					<svg class="h-5 w-5 text-accent-green-500" fill="currentColor" viewBox="0 0 20 20">
						<path
							fill-rule="evenodd"
							d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
							clip-rule="evenodd"
						></path>
					</svg>
					<span>Privacy-focused</span>
				</div>
			</div>
		</div>
	</div>
</section>

