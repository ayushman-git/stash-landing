<section class="relative bg-dark-green-900/20 py-24">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<!-- Section header -->
		<div class="mb-16 text-center">
			<h2 class="mb-4 font-['Inter'] text-4xl font-bold text-white sm:text-5xl">
				Two ways to use Stash
			</h2>
		</div>

		<!-- Use cases grid -->
		<div class="grid gap-12 lg:grid-cols-2">
			<!-- Quick Save -->
			<div
				class="rounded-2xl border border-dark-green-700/30 bg-dark-green-900/40 p-8 backdrop-blur-sm"
			>
				<div class="mb-6">
					<h3 class="mb-3 text-2xl font-bold text-white">Quick Save</h3>
					<p class="text-lg text-gray-400">
						Simple workflow for saving articles from your browser
					</p>
				</div>

				<div class="space-y-4">
					<div class="flex items-start gap-4">
						<div
							class="flex h-8 w-8 flex-shrink-0 items-center justify-center rounded-full bg-accent-green-500/20 text-sm font-semibold text-accent-green-400"
						>
							1
						</div>
						<div>
							<p class="text-white">Copy URL from browser</p>
							<p class="text-sm text-gray-500">⌘+C or Ctrl+C</p>
						</div>
					</div>

					<div class="flex items-start gap-4">
						<div
							class="flex h-8 w-8 flex-shrink-0 items-center justify-center rounded-full bg-accent-green-500/20 text-sm font-semibold text-accent-green-400"
						>
							2
						</div>
						<div>
							<p class="text-white">Run stash add</p>
							<code class="text-sm text-accent-green-400">stash add --from-clipboard</code>
						</div>
					</div>

					<div class="flex items-start gap-4">
						<div
							class="flex h-8 w-8 flex-shrink-0 items-center justify-center rounded-full bg-accent-green-500/20 text-sm font-semibold text-accent-green-400"
						>
							3
						</div>
						<div>
							<p class="text-white">Done! Article saved locally</p>
							<p class="text-sm text-gray-500">Read it anytime with stash open</p>
						</div>
					</div>
				</div>

				<div class="mt-8">
					<div class="terminal-window">
						<div class="terminal-header">
							<div class="terminal-dot bg-red-500"></div>
							<div class="terminal-dot bg-yellow-500"></div>
							<div class="terminal-dot bg-green-500"></div>
						</div>
						<div class="terminal-body text-sm">
							<div><span class="token-command">$ stash add</span> <span class="token-flag">--from-clipboard</span></div>
							<div class="mt-2 text-gray-400">✓ Saved: Building CLI Tools</div>
							<div class="text-gray-500">  ID: 42</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Power User -->
			<div
				class="rounded-2xl border border-dark-green-700/30 bg-dark-green-900/40 p-8 backdrop-blur-sm"
			>
				<div class="mb-6">
					<h3 class="mb-3 text-2xl font-bold text-white">Power User</h3>
					<p class="text-lg text-gray-400">Advanced features for organizing and discovering content</p>
				</div>

				<div class="space-y-4">
					<div class="flex items-start gap-4">
						<div
							class="flex h-8 w-8 flex-shrink-0 items-center justify-center rounded-full bg-accent-green-500/20 text-sm font-semibold text-accent-green-400"
						>
							🏷️
						</div>
						<div>
							<p class="text-white">Tag and organize</p>
							<p class="text-sm text-gray-500">Auto-tagging by domain + custom tags</p>
						</div>
					</div>

					<div class="flex items-start gap-4">
						<div
							class="flex h-8 w-8 flex-shrink-0 items-center justify-center rounded-full bg-accent-green-500/20 text-sm font-semibold text-accent-green-400"
						>
							🔍
						</div>
						<div>
							<p class="text-white">Full-text search</p>
							<p class="text-sm text-gray-500">Search across titles, content, and tags</p>
						</div>
					</div>

					<div class="flex items-start gap-4">
						<div
							class="flex h-8 w-8 flex-shrink-0 items-center justify-center rounded-full bg-accent-green-500/20 text-sm font-semibold text-accent-green-400"
						>
							⚡
						</div>
						<div>
							<p class="text-white">Fuzzy finding</p>
							<p class="text-sm text-gray-500">Interactive picker with fzf integration</p>
						</div>
					</div>
				</div>

				<div class="mt-8">
					<div class="terminal-window">
						<div class="terminal-header">
							<div class="terminal-dot bg-red-500"></div>
							<div class="terminal-dot bg-yellow-500"></div>
							<div class="terminal-dot bg-green-500"></div>
						</div>
						<div class="terminal-body text-sm">
							<div><span class="token-command">$ stash pick</span></div>
							<div class="mt-2 text-gray-400">> rust</div>
							<div class="text-accent-green-400">▸ Building CLI Tools in Rust</div>
							<div class="text-gray-400">  Async Programming Guide</div>
							<div class="text-gray-400">  Rust 1.82.0 Release</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

