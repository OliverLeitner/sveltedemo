<script lang="ts">
    export let name: string;
</script>

<main>
	<h1>Hello {name}</h1>
    <!-- below goes the countent from the router -->
    <slot></slot>
</main>