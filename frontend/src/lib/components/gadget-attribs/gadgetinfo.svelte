<script>
	import Monaco from '../monaco.svelte';

	let { gadgetInfo } = $props();

	let gadgetInfoSource = $state('');
	$effect(() => {
		console.log('new src');
		gadgetInfoSource = JSON.stringify(gadgetInfo, null, '  ');
	});
</script>

<Monaco content={gadgetInfoSource} readOnly={true} />
