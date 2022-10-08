<script lang=ts>
	import Card from "./Card.svelte";

	const cardEmojis = [
		'\u{1F984}',
		'\u{1F47B}',
		'\u{1F984}',
		'\u{1F47B}'
	]
</script>

<div class='card-container'>
{#each cardEmojis as emoji}
	<Card emoji={emoji} />
{/each}
</div>

<style>
	.card-container {
		display: flex;
		gap: 8px;
	}
</style>