<script lang=ts>
	import Card from "./Card.svelte";

	const emojis = [
		'\u{1F98A}',
		'\u{1F984}',
		'\u{1F47B}']

	const cards = [...emojis, ...emojis];

	const shuffle = (deck: string[]) => {
		const newDeck = [...deck]
		const idx1 = Math.floor(Math.random() * deck.length)
		const idx2 = Math.floor(Math.random() * deck.length)
		newDeck[idx1] = deck[idx2]
		newDeck[idx2] = deck[idx1]
		return newDeck;
	}

	let shuffledCards = cards;
	for (let i = 0; i < 20 ; i++) {
		shuffledCards = shuffle(shuffledCards)
	}

</script>

<div class='card-container'>
{#each shuffledCards as emoji}
	<Card emoji={emoji} />
{/each}
</div>

<style>
	.card-container {
		display: flex;
		gap: 8px;
	}
</style>