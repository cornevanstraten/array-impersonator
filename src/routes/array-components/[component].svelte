<script context="module">
	//a script with context module will be loaded before the page is rendered (SSR)
	export async function load({ params }) {
		const componentName = params.component;
		return { props: { componentName } };
	}
</script>

<script>
	import CreditReport from '../../components/credit-report.svelte';
	export let componentName;
</script>

<h1 class="text-4xl text-center mt-8 lowercase">{componentName}</h1>

{#if componentName === 'credit-report'}
	<CreditReport />
{/if}
