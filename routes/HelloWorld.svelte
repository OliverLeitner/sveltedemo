<script lang="ts">
    import axios from "axios";
	import HelloWorld from "../controller/HelloWorld.svelte"
	export let name: string; // lets place var from app.svelte into controller helloworld...

	import { onMount } from "svelte";
    let non = [];
    // let gettingQuote = false;

    onMount(() => {
        getRandomQuote();
    });

    async function getRandomQuote() {
        // gettingQuote = true;
        //const res = await fetch("https://api.quotable.io/random");
        const res = await axios.get("https://api.ip2country.info/ip?5.6.7.8")
        const json = await res.data;
        // non = [...non, json];
        non = json
        // gettingQuote = false;
    }

  /*import { onMount } from "svelte";
  let mytodo;

  onMount(
      fetch("https://jsonplaceholder.typicode.com/todos/1")
      .then(response => response.json())
      .then(todo => {
          mytodo = todo;
      })  
      );
      */
</script>

<HelloWorld name={name}>
	<!--div>
        {#each non as {author, content}}
            <p>{content} - {author}</p>
        {/each}
        <button on:click={getRandomQuote} disabled={gettingQuote}>Get Quote</button>
        {#if gettingQuote}
            <span>Getting Quote...</span>
        {/if}
    </div-->
    <div>
        {#if non["countryCode"]}
          <ul>
            <li>{non["countryName"]}</li>
          </ul>
        {:else}
          <p>loading.....</p>
        {/if}
      </div>
</HelloWorld>

<style>
	p {
		color: red;
		font-weight: bold;
	}
</style>