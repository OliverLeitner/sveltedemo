<script lang="ts">
	import HelloWorld from "../controller/HelloWorld.svelte"
	export let name: string; // lets place var from app.svelte into controller helloworld...
</script>

<HelloWorld name={name}>
	<p>some slot content</p>
</HelloWorld>

<style>
	p {
		color: red;
		font-weight: bold;
	}
</style>