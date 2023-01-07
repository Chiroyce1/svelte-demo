<script lang="ts">
	let text: String;

	function handleClick() {
		location.href = `/test/${text}`;
	}
</script>

<style>
	a { color: black; }
</style>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<input type="text" bind:value={text}>
<a href={`/test/${text}`}><button>Load</button></a>