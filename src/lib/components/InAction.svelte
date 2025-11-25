<script lang="ts">
	// Workflows with personality
</script>

<section class="bg-bg-secondary py-16 md:py-64">
	<div class="mx-auto max-w-(--max-content) px-6">
		<!-- Section header -->
		<div class="mb-16 max-w-2xl">
			<p class="mb-3 font-mono text-sm text-text-muted">// real workflows, not marketing demos</p>
			<h2 class="heading-section text-text-primary">Copy. Paste. Done.</h2>
		</div>

		<!-- Workflows -->
		<div class="space-y-20 md:space-y-28">
			<!-- Workflow 1: Save -->
			<div class="grid items-center gap-8 md:grid-cols-2 md:gap-12">
				<div>
					<p class="mb-2 font-mono text-sm text-accent">stash add &lt;url&gt;</p>
					<h3 class="mb-4 text-2xl font-semibold text-text-primary tracking-tight">
						URL in, article saved.
					</h3>
					<p class="mb-4 text-text-secondary leading-relaxed">
						No browser extension. No "save to..." menu. Just paste a URL and stash fetches 
						the title, extracts the content, and stores it as clean Markdown.
					</p>
					<p class="font-mono text-sm text-text-muted">
						Works with paywalled sites too. If you can read it, stash can save it.
					</p>
				</div>
				<div class="terminal-window">
					<div class="terminal-header">
						<div class="terminal-dot bg-terminal-dot-red"></div>
						<div class="terminal-dot bg-terminal-dot-yellow"></div>
						<div class="terminal-dot bg-terminal-dot-green"></div>
					</div>
					<div class="terminal-body">
						<div class="mb-1 token-comment"># That article you've been meaning to read</div>
						<div class="mb-3">
							<span class="token-command">$ stash add</span>
							<span class="token-arg"> https://brandur.org/nanoglyphs/044-ghosts</span>
							<span class="token-flag"> #essays</span>
						</div>
						<div class="mb-1 token-success">✓ Saved: Ghosts · Nanoglyph 044</div>
						<div class="text-text-muted">  ID: 127 • brandur.org • 8 min read</div>
					</div>
				</div>
			</div>

			<!-- Workflow 2: Find -->
			<div class="grid items-center gap-8 md:grid-cols-2 md:gap-12">
				<div class="md:order-2">
					<p class="mb-2 font-mono text-sm text-accent">stash pick | stash search</p>
					<h3 class="mb-4 text-2xl font-semibold text-text-primary tracking-tight">
						Find it before you finish typing.
					</h3>
					<p class="mb-4 text-text-secondary leading-relaxed">
						Fuzzy search across titles, tags, and full content. Start typing and results 
						appear instantly. Pipe to fzf for the full interactive experience.
					</p>
					<div class="flex flex-wrap gap-2 font-mono text-xs">
						<span class="rounded bg-bg-tertiary px-2 py-1 text-text-muted">stash ls --tag rust</span>
						<span class="rounded bg-bg-tertiary px-2 py-1 text-text-muted">stash search "async"</span>
						<span class="rounded bg-bg-tertiary px-2 py-1 text-text-muted">stash pick | fzf</span>
					</div>
				</div>
				<div class="md:order-1">
					<div class="terminal-window">
						<div class="terminal-header">
							<div class="terminal-dot bg-terminal-dot-red"></div>
							<div class="terminal-dot bg-terminal-dot-yellow"></div>
							<div class="terminal-dot bg-terminal-dot-green"></div>
						</div>
						<div class="terminal-body">
							<div class="mb-1 token-comment"># What was that article about...</div>
							<div class="mb-3">
								<span class="token-command">$ stash search</span>
								<span class="token-arg"> "rust async"</span>
							</div>
							<div class="text-text-secondary">
								<div class="mb-1"><span class="text-accent">127</span> Ghosts · Nanoglyph 044 <span class="text-text-muted">• essays</span></div>
								<div class="mb-1"><span class="text-accent">98</span> Async Rust Is Hard <span class="text-text-muted">• rust, async</span></div>
								<div><span class="text-accent">84</span> Tokio Tutorial <span class="text-text-muted">• rust, tutorial</span></div>
							</div>
						</div>
					</div>
				</div>
			</div>

			<!-- Workflow 3: Read -->
			<div class="grid items-center gap-8 md:grid-cols-2 md:gap-12">
				<div>
					<p class="mb-2 font-mono text-sm text-accent">stash read &lt;id&gt;</p>
					<h3 class="mb-4 text-2xl font-semibold text-text-primary tracking-tight">
						Read it. Finally.
					</h3>
					<p class="mb-4 text-text-secondary leading-relaxed">
						Opens in your terminal with your pager of choice. Clean Markdown, no ads, 
						no cookie banners, no "subscribe to continue reading" popups.
					</p>
					<p class="font-mono text-sm text-text-muted">
						Export to PDF, epub, or just cat it to stdout. Your content, your rules.
					</p>
				</div>
				<div class="terminal-window">
					<div class="terminal-header">
						<div class="terminal-dot bg-terminal-dot-red"></div>
						<div class="terminal-dot bg-terminal-dot-yellow"></div>
						<div class="terminal-dot bg-terminal-dot-green"></div>
					</div>
					<div class="terminal-body">
						<div class="mb-1 token-comment"># Time to actually read it</div>
						<div class="mb-3">
							<span class="token-command">$ stash read</span>
							<span class="token-arg"> 127</span>
						</div>
						<div class="border-l-2 border-accent/30 pl-4">
							<div class="mb-2 text-lg font-semibold text-text-primary">Ghosts · Nanoglyph 044</div>
							<div class="mb-3 text-text-muted text-xs">brandur.org • 8 min read • saved 2 days ago</div>
							<div class="text-text-secondary text-sm leading-relaxed">
								I've been mass-unsubscribing from newsletters. 
								Not because they're bad, but because I never 
								read them...
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>

		<!-- Bottom CTA hint -->
		<div class="mt-20 text-center">
			<p class="font-mono text-sm text-text-muted">
				<span class="text-accent">$</span> stash --help <span class="text-text-muted">← there's more where this came from</span>
			</p>
		</div>
	</div>
</section>

