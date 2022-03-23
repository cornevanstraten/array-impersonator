<script>
	// @ts-nocheck
	import { onMount } from 'svelte';
	import { appKey, userToken } from '../stores/keys';

	// function setScripts() {
	// 	if (document) {
	// 		// update script imports arrayScript1 and arrayScript2
	// 		document.getElementById(
	// 			'arrayScript1'
	// 		).src = `https://embed.array.io/cms/array-web-component.js?appKey=${$appKey}`;
	// 		document.getElementById(
	// 			'arrayScript2'
	// 		).src = `https://embed.array.io/cms/array-credit-report.js?appKey=${$appKey}`;

	// 	}
	// }
	// onMount(async () => {
	// 	setScripts();
	// });

	$: {
		console.log(`appKey: ${$appKey}`);
		console.log(`userToken: ${$userToken}`);
	}
</script>

<svelte:head>
	<title>array test components</title>
</svelte:head>

<h1 class="text-4xl text-center mt-8 lowercase">array test components v0.0.1</h1>
<p class="text-lg text-center mb-8 text-gray-300">powered by Svelte</p>

<div class="">
	<div class="my-6">
		<label for="">appKey</label>
		<input
			class="w-full rounded-md p-4 border-2 border-gray-200"
			type="text"
			placeholder="Enter appKey"
			bind:value={$appKey}
		/>
		<a
			class="text-xs text-blue-400"
			href="https://metabase.internal.array.io/question/406-find-appkey"
			target="_blank">Find appKey with clientKey (Metabase)</a
		>
	</div>

	<div class="my-6">
		<label for="">userToken</label>
		<input
			class="w-full rounded-md p-4 border-2 border-gray-200"
			type="text"
			placeholder="Enter userToken"
			bind:value={$userToken}
		/>
		<a
			class="text-xs text-blue-400"
			href="https://metabase.internal.array.io/question/363-usertoken"
			target="_blank">Find userToken with clientKey (Metabase)</a
		>
		<br />
		<a
			class="text-xs text-blue-400"
			href="https://portal.systemadmin.com/ccp_report_credmo_client_token.asp"
			target="_blank">Extend userToken (SystemAdmin)</a
		>
	</div>
</div>

<h2 class="text-xl">Components</h2>

<ul>
	<li><a href={`/array-components/credit-report`} class="text-blue-400">Credit-Report</a></li>
</ul>
