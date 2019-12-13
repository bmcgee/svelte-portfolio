<script>
	import Item from './Item.svelte';
	let visible = false;
	export let items = [];

</script>

<nav>
<ul>
	{#each items as item, i}
		<Item index={i+1} title={item.name} content={item.content}/>
	{/each}
</ul>


</nav>

<style>

</style>
