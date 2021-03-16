<script lang="ts">
    export let name: string;

  	/*export let mytodo = fetch("https://jsonplaceholder.typescript.com/todos/1")
      .then(response => response.json())
      .then(todo => {
          mytodo = todo;
    })*/

    /*import { onMount } from "svelte";
    let non = [];
    let gettingQuote = false;

    onMount(() => {
        getRandomQuote();
    });

    async function getRandomQuote() {
        gettingQuote = true;
        const res = await fetch("https://api.quotable.io/random");
        const json = await res.json();
        non = [...non, json];
        gettingQuote = false;
    }*/
</script>

<main>
	<h1>Hello {name}</h1>
    <!-- below goes the countent from the router -->
    <slot></slot>
</main>