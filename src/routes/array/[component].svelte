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

{#if componentName === 'credit-overview'}
	<array-credit-overview appKey={$appKey} userToken={$userToken} defaultBureau="all" />
{/if}

{#if componentName === 'credit-alerts'}
	<array-credit-alerts
		appKey={$appKey}
		userToken={$userToken}
		maxPages="10"
		alertsPerPage="10"
		bureau="all"
		defaultBureau="all"
	/>
{/if}
{#if componentName === 'account-settings'}
	<array-account-settings appKey={$appKey} userToken={$userToken} startPage="personalInformation" />
{/if}
