<script lang="ts">
	import { Bookmark, Cloud, Clock, Code } from 'lucide-svelte';

	const problems = [
		{
			icon: Bookmark,
			text: 'People save 100 articles but read 0'
		},
		{
			icon: Cloud,
			text: 'Browser bookmarks are messy chaos'
		},
		{
			icon: Clock,
			text: 'Pocket and Instapaper are slow or cloud-locked'
		},
		{
			icon: Code,
			text: 'Developers want something fast, local, scriptable'
		}
	];
</script>

<section class="bg-bg-primary py-16 md:py-24">
	<div class="mx-auto max-w-(--max-content) px-6">
		<div class="mx-auto max-w-(--max-narrow)">
			<!-- Section header -->
			<h2 class="heading-section mb-10 text-center text-text-primary">
				The problem
			</h2>

			<!-- Problem list -->
			<div class="space-y-4">
				{#each problems as problem}
					<div class="flex items-start gap-4 rounded border border-border bg-bg-secondary p-5">
						<div class="shrink-0 text-text-muted">
							<problem.icon size={20} strokeWidth={1.5} />
						</div>
						<p class="body-base text-text-secondary">{problem.text}</p>
					</div>
				{/each}
			</div>

			<!-- Empathy line -->
			<p class="mt-8 text-center text-text-muted font-mono text-sm">
				We understand. You're not alone.
			</p>
		</div>
	</div>
</section>
