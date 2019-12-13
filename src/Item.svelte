<script context="module">
	const elements = new Set();

	export function hideAll() {
		elements.forEach(element => {
			element.toggleVis();
		});
	}
</script>

<script>
	import { onMount } from 'svelte';
	import Project from './Project.svelte';

	export let title;
	export let index;
	export let content;

	let project;
	onMount(() => {
		elements.add(project);
		return () => elements.delete(project);
	});

	function hideOthers() {
		console.log(elements);
		elements.forEach(element => {
		if (element == project) element.setVisible();
		if (element !== project) element.setInvisible();
	});
	}


</script>

<page>

	<li
	on:click={hideOthers}>{index} {title}
	<Project content={content} bind:this={project} />
	</li>
</page>
