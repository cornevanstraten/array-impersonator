<script>
	// @ts-nocheck
	import { appKey, userToken } from '../stores/keys';

	import creditReportImage from '../../static/credit-report.png';
	import scoreSimulatorImage from '../../static/score-simulator.png';
	import scoreSightImage from '../../static/score-sight.png';
	import creditOverviewImage from '../../static/credit-overview.png';
	import creditAlertsImage from '../../static/credit-alerts.png';
	import accountSettingsImage from '../../static/account-settings.png';

	$: {
		console.log(`appKey: ${$appKey}`);
		console.log(`userToken: ${$userToken}`);
	}
</script>

<svelte:head>
	<title>array impersonator</title>
</svelte:head>

<div class="max-w-xl mx-auto">
	<h1 class="text-4xl text-center mt-8 lowercase">array impersonator v0.0.1</h1>
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

	<h2 class="text-xl my-8">Components</h2>

	<div class="grid grid-cols-3 gap-4 text-center">
		<component class="overflow-hidden rounded-lg shadow-md hover:shadow-xl bg-gray-100">
			<a href={`/array/credit-report`}>
				<img class="block h-auto w-full" src={creditReportImage} alt="credit-report" />
			</a>
			<h1 class="text-lg text-center p-2">Credit Report</h1>
		</component>
		<component class="overflow-hidden rounded-lg shadow-md hover:shadow-xl bg-gray-100">
			<a href={`/array/credit-score-simulator`}>
				<img class="block h-auto w-full" src={scoreSimulatorImage} alt="credit-score-simulator" />
			</a>
			<h1 class="text-lg text-center p-2">Score Simulator</h1>
		</component>
		<component class="overflow-hidden rounded-lg shadow-md hover:shadow-xl bg-gray-100">
			<a href={`/array/credit-score-sight`}>
				<img class="block h-auto w-full" src={scoreSightImage} alt="credit-score-sight" />
			</a>
			<h1 class="text-lg text-center p-2">Score Sight</h1>
		</component>
		<component class="overflow-hidden rounded-lg shadow-md hover:shadow-xl bg-gray-100">
			<a href={`/array/credit-overview`}>
				<img class="block h-auto w-full" src={creditOverviewImage} alt="credit-overview" />
			</a>
			<h1 class="text-lg text-center p-2">Credit Overview</h1>
		</component>
		<component class="overflow-hidden rounded-lg shadow-md hover:shadow-xl bg-gray-100">
			<a href={`/array/credit-alerts`}>
				<img class="block h-auto w-full" src={creditAlertsImage} alt="credit-alerts" />
			</a>
			<h1 class="text-lg text-center p-2">Credit Alerts</h1>
		</component>
		<component class="overflow-hidden rounded-lg shadow-md hover:shadow-xl bg-gray-100">
			<a href={`/array/account-settings`}>
				<img class="block h-auto w-full" src={accountSettingsImage} alt="account-settings" />
			</a>
			<h1 class="text-lg text-center p-2">Account settings</h1>
		</component>
	</div>
</div>
