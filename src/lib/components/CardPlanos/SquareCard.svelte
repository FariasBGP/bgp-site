<script lang="ts">
	import CardBody from './BodyCard.svelte';
	import CardIcon from './CardIcon.svelte';

	interface Card {
		img: string;
		titulo: string;
		topicos: string[];
	}
	export let card: Card;
</script>

<div
	class=" relative flex h-full border border-dashed border-secondary-foreground/50 bg-background"
>
	{#each ['-left-3 -top-3', '-right-3 -top-3', '-bottom-3 -left-3', '-bottom-3 -right-3'] as position}
		<CardIcon class={position} />
	{/each}
	<CardBody className="px-5 relative py-10" {card} />
</div>
