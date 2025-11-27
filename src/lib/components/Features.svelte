<script lang="ts">
	// No icons needed - typography-driven design
</script>

<section class="bg-bg-primary py-16 md:py-24">
	<div class="mx-auto max-w-(--max-content) px-6 mb-64">
		<!-- Section header -->
		<div class="mb-16 max-w-2xl">
			<p class="mb-3 font-mono text-sm text-text-muted">// the boring-but-important stuff</p>
			<h2 class="heading-section text-text-primary">
				No magic. Just good defaults.
			</h2>
		</div>

		<!-- Features - asymmetric layout -->
		<div class="grid gap-6 lg:grid-cols-2">
			<!-- Hero feature - Rust performance -->
			<div class="relative overflow-hidden rounded border border-border bg-bg-secondary p-8 lg:row-span-2">
				<div class="mb-6">
					<h3 class="mb-1 font-mono text-sm text-accent">Rust = instant</h3>
					<p class="text-2xl font-semibold text-text-primary tracking-tight">12ms</p>
				</div>
				<p class="mb-6 text-text-secondary leading-relaxed">
					Since stash is made on Rust, it's super fast and responsive.
					Most of the commands execute in under 20 milliseconds, even with thousands of articles.
				</p>
				<div class="rounded bg-bg-tertiary p-4 font-mono text-sm">
					<div class="text-text-muted mb-2">$ time stash ls</div>
					<div class="text-text-secondary mb-1">42 ★ Announcing Rust 1.82.0</div>
					<div class="text-text-secondary mb-1">41 &nbsp; Building CLI Tools in Rust</div>
					<div class="text-text-secondary mb-3">40 &nbsp; The Art of Command Line</div>
					<div class="text-text-muted">real &nbsp; <span class="text-accent">0m0.012s</span></div>
				</div>
			</div>

			<!-- Your machine, your data -->
			<div class="rounded border border-border bg-bg-secondary p-8">
				<div class="mb-4">
					<h3 class="mb-1 font-mono text-sm text-accent">~/.local/share/stash/</h3>
					<p class="text-xl font-semibold text-text-primary tracking-tight">Your machine. Your data.</p>
				</div>
				<p class="text-text-secondary leading-relaxed">
					One SQLite file. No account creation.
					Delete the folder and it's gone. Back it up and it's safe.
				</p>
			</div>

			<!-- Git sync -->
			<div class="rounded border border-border bg-bg-secondary p-8">
				<div class="mb-4">
					<h3 class="mb-1 font-mono text-sm text-accent">git push = synced</h3>
					<p class="text-xl font-semibold text-text-primary tracking-tight">Version control for your reading list.</p>
				</div>
				<p class="mb-4 text-text-secondary leading-relaxed">
					The database is just a file. Throw it in a git repo. 
					Now you have history, branches, and sync across machines.
				</p>
				<div class="flex flex-wrap gap-2 font-mono text-xs">
					<span class="rounded bg-bg-tertiary px-2 py-1 text-text-muted">git diff</span>
					<span class="rounded bg-bg-tertiary px-2 py-1 text-text-muted">git log</span>
					<span class="rounded bg-bg-tertiary px-2 py-1 text-text-muted">git checkout</span>
				</div>
			</div>
		</div>

		<!-- Bottom row - smaller feature cards -->
		<div class="mt-6 grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
			<div class="rounded border border-border bg-bg-secondary p-6">
				<p class="mb-2 font-semibold text-text-primary">TUI included</p>
				<p class="text-sm text-text-secondary">
					If you don't like typing commands, there's a full terminal UI built-in. Just run <code class="rounded bg-bg-tertiary px-1 text-xs">stash tui</code>.
				</p>
			</div>
			<div class="rounded border border-border bg-bg-secondary p-6">
				<p class="mb-2 font-semibold text-text-primary">fzf → fuzzy everything</p>
				<p class="text-sm text-text-secondary">
					Pipe to fzf, grep through content, script your workflows. Built for devs.
				</p>
			</div>
			<div class="rounded border border-border bg-bg-secondary p-6">
				<p class="mb-2 font-semibold text-text-primary">#tags that actually work</p>
				<p class="text-sm text-text-secondary">
					Auto-tagged by domain. Add your own. Search across everything with 
					<code class="rounded bg-bg-tertiary px-1 text-xs">stash search</code>.
				</p>
			</div>
		</div>
	</div>
</section>

