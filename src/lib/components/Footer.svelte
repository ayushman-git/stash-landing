<script lang="ts">
	import { Github } from 'lucide-svelte';
</script>

<footer class="border-t border-border bg-bg-primary py-12 md:py-16">
	<div class="mx-auto max-w-(--max-content) px-6">
		<div class="grid gap-10 sm:grid-cols-2 lg:grid-cols-3">
			<!-- About -->
			<div>
				<h3 class="mb-4 font-semibold text-text-primary">Stash</h3>
				<p class="text-sm leading-relaxed text-text-secondary">
					Fast, local-first CLI tool for managing your reading list. Built with Rust for speed and
					reliability.
				</p>
			</div>

			<!-- Resources -->
			<div>
				<h3 class="mb-4 font-semibold text-text-primary">Resources</h3>
				<ul class="space-y-2 text-sm">
					<li>
						<a
							href="https://github.com/ayushman-git/stash"
							class="text-text-secondary transition-colors hover:text-accent"
						>
							Documentation
						</a>
					</li>
					<li>
						<a
							href="https://github.com/ayushman-git/stash/releases"
							class="text-text-secondary transition-colors hover:text-accent"
						>
							Releases
						</a>
					</li>
				</ul>
			</div>

			<!-- Community -->
			<div>
				<h3 class="mb-4 font-semibold text-text-primary">Community</h3>
				<ul class="space-y-2 text-sm">
					<li>
						<a
							href="https://github.com/ayushman-git/stash"
							class="text-text-secondary transition-colors hover:text-accent"
						>
							GitHub
						</a>
					</li>
					<li>
						<a
							href="https://github.com/ayushman-git/stash/issues"
							class="text-text-secondary transition-colors hover:text-accent"
						>
							Issues
						</a>
					</li>
					<li>
						<a
							href="https://github.com/ayushman-git/stash/blob/main/CONTRIBUTING.md"
							class="text-text-secondary transition-colors hover:text-accent"
						>
							Contributing
						</a>
					</li>
				</ul>
			</div>
		</div>

		<!-- Bottom bar -->
		<div
			class="mt-10 flex flex-col items-center justify-between gap-4 border-t border-border pt-8 text-sm text-text-muted sm:flex-row"
		>
			<p>© 2025 Stash. MIT License.</p>
			<a
				href="https://github.com/ayushman-git/stash"
				class="text-text-muted transition-colors hover:text-accent"
				aria-label="GitHub"
			>
				<Github size={20} strokeWidth={1.5} />
			</a>
		</div>
	</div>
</footer>

