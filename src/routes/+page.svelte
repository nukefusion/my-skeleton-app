<script>
	import ValueSource from '../lib/valueSource.svelte';
	import StopsRender from '../lib/stopsRender.svelte';
	import { ConicGradient } from '@skeletonlabs/skeleton';

	export let values;

	$: conicStops = [{ color: 'red', start: 0, end: values?.start1 || 0 },
		{ color: 'yellow', start: values?.start1 || 0, end: values?.start2 || 0 },
		{ color: 'blue', start: values?.start2 || 0, end: 100 }];
</script>

<ValueSource bind:values></ValueSource>
<ConicGradient stops={conicStops} width="w-16"></ConicGradient>
<StopsRender stops={conicStops}></StopsRender>

