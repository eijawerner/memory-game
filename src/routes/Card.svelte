<script lang="ts">
	export let emoji: string;
    let hidden = true;
</script>

<button class={`card ${hidden? "hidden" : ''}`} on:click={() => (hidden = !hidden)}>
    {hidden? "" : emoji}
</button>

<style>
    .card {
        font-size: 4em;
        background: lightblue;
        height: 120px;
        width: 100px;
        border-radius: 8px;
    }
    .card.hidden {
        background: lightseagreen;
    }
</style>