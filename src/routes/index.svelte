<script>
	export let id;
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section>
	<h1>Homepage</h1>
	<a href="/visit?id=1">Visit 1</a>
	<a href="/visit?id=2">Visit 2</a>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}
</style>
