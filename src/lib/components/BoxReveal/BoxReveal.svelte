<script>
	import { inview } from 'svelte-inview';
	import { Motion, useAnimation } from 'svelte-motion';

	export let width = 'fit-content';
	export let boxColor = '#CB3E38';
	export let duration = 0.5;

	// Animation Controls
	const mainControls = useAnimation();
	const sideControls = useAnimation();

	const viewEnter = () => {
		mainControls.start('visible');
		sideControls.start('visible');
	};
</script>

<div class="relative overflow-hidden" style="width:{width}" use:inview on:inview_enter={viewEnter}>
	<Motion
		let:motion
		variants={{
			hidden: { opacity: 0, y: 75 },
			visible: { opacity: 1, y: 0 }
		}}
		initial="hidden"
		animate={mainControls}
		transition={{ duration, delay: 0.25 }}
	>
		<div use:motion>
			<slot>Default</slot>
		</div>
	</Motion>
	<Motion
		variants={{
			hidden: { left: 0 },
			visible: { left: '100%' }
		}}
		initial="hidden"
		animate={sideControls}
		transition={{ duration, ease: 'easeIn' }}
		let:motion
	>
		<div
			style="background:{boxColor}"
			class="absolute bottom-[4px] left-0 right-0 top-[4px] z-40"
			use:motion
		></div>
	</Motion>
</div>
