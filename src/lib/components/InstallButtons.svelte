<script lang="ts">
	let copied = $state('');

	const platforms = [
		{ name: 'macOS', command: 'brew install stash', icon: '🍎' },
		{ name: 'Windows', command: 'winget install stash', icon: '🪟' },
		{ name: 'Linux', command: 'curl -sSL https://stash.sh/install.sh | sh', icon: '🐧' }
	];

	async function copyToClipboard(command: string, platform: string) {
		try {
			await navigator.clipboard.writeText(command);
			copied = platform;
			setTimeout(() => {
				copied = '';
			}, 2000);
		} catch (err) {
			console.error('Failed to copy:', err);
		}
	}
</script>

<div class="flex flex-col gap-4 sm:flex-row sm:gap-6">
	{#each platforms as platform}
		<button
			onclick={() => copyToClipboard(platform.command, platform.name)}
			class="group relative flex items-center gap-3 rounded-lg border border-dark-green-700/30 bg-dark-green-900/50 px-6 py-4 backdrop-blur-sm transition-all hover:border-accent-green-500/50 hover:bg-dark-green-800/50"
		>
			<span class="text-2xl">{platform.icon}</span>
			<div class="flex-1 text-left">
				<div class="text-sm font-medium text-accent-green-400">{platform.name}</div>
				<code class="text-xs text-gray-400">{platform.command}</code>
			</div>
			<div class="text-gray-400 transition-colors group-hover:text-accent-green-400">
				{#if copied === platform.name}
					<svg class="h-5 w-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M5 13l4 4L19 7"
						></path>
					</svg>
				{:else}
					<svg class="h-5 w-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"
						></path>
					</svg>
				{/if}
			</div>
		</button>
	{/each}
</div>

