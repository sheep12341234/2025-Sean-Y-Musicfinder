<script>
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>
<style>
	nav {
		background: gray;
		padding: 10px;
	}

	nav a{
		color:white;
	}
</style>
<nav>
	<a href = "/">home</a>
	<a href = "/about">about</a>
</nav>
{@render children?.()}