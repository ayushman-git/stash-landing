<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import Problem from '$lib/components/Problem.svelte';
	import Solution from '$lib/components/Solution.svelte';
	import Features from '$lib/components/Features.svelte';
	import InAction from '$lib/components/InAction.svelte';
	import Installation from '$lib/components/Installation.svelte';
	import WhyThisTool from '$lib/components/WhyThisTool.svelte';
	import FAQ from '$lib/components/FAQ.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<div class="min-h-screen bg-bg-primary text-text-primary">
	<Hero />
	<Problem />
	<Solution />
	<Features />
	<InAction />
	<Installation />
	<WhyThisTool />
	<FAQ />
	<Footer />
</div>
