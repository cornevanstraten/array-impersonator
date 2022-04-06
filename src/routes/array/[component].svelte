<script context="module">
	//a script with context module will be loaded before the page is rendered (SSR)
	export async function load({ params }) {
		const componentName = params.component;
		return { props: { componentName } };
	}
</script>

<script>
	export let componentName;
	import { appKey, userToken } from '../../stores/keys';
</script>

{#if componentName === 'credit-report'}
	<array-credit-report appKey={$appKey} userToken={$userToken} />
{/if}

{#if componentName === 'credit-score-simulator'}
	<array-credit-score-simulator appKey={$appKey} userToken={$userToken} />
{/if}

{#if componentName === 'credit-score-sight'}
	<array-credit-score-sight appKey={$appKey} userToken={$userToken} />
{/if}
