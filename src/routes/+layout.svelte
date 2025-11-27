<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	
	let { children } = $props();
</script>

<svelte:head>
	<title>Stash - Your Local-First Article Manager</title>
	<meta name="description" content="Fast, local-first CLI tool for saving, organizing, and reading articles. Built in Rust for speed and privacy. Your articles, your way." />
	<meta name="keywords" content="CLI, article manager, Rust, local-first, privacy, offline reading, developer tools" />
	
	<!-- Open Graph / Facebook -->
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Stash - Your Local-First Article Manager" />
	<meta property="og:description" content="Fast, local-first CLI tool for saving, organizing, and reading articles. Built in Rust for speed and privacy." />
	
	<!-- Twitter -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="Stash - Your Local-First Article Manager" />
	<meta name="twitter:description" content="Fast, local-first CLI tool for saving, organizing, and reading articles. Built in Rust for speed and privacy." />
	
	<!-- Favicon -->
	<link rel="icon" href={favicon} />
	
	<!-- Fonts -->
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet" />

	<script defer src="https://cloud.umami.is/script.js" data-website-id="f5602a52-acb3-4eb2-b455-b3f7084a3994"></script>
</svelte:head>

{@render children()}
