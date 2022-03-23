<script>
	import { appKey, userToken } from '../stores/keys';
</script>

<p>appKey: {$appKey}</p>
<p>userToken: {$userToken}</p>

<array-credit-report
	appKey={$appKey}
	userToken={$userToken}
	live="true"
	productCode="credmo3bReportScore"
/>
