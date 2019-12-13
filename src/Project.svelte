

<script>
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';
	import Red from './Red.svelte'

	export let content;
	export let visible = false;

	export function setVisible() {
		visible = true;
	}

	export function setInvisible() {
		visible = false;
	}

</script>

<project>
	{#if visible}
	<p transition:fade>{@html content}</p>
	{/if}
</project>
