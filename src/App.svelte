<script>
	import Intro from './Intro.svelte';
	import Nav from './Nav.svelte';
	import data from './pages/*'
</script>

<main>
	<Intro />
	<Nav items={data} />

</main>

<style>

</style>
