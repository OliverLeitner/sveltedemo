<script lang="ts">
	import { Router, Link, Route } from "svelte-routing";
  	import Home from "../routes/Home.svelte";
	import HelloWorld from "../routes/HelloWorld.svelte";
  	export let url = "";
	import "../css/default.css"; // global styles
</script>

<Router url="{url}">
	<nav>
	  <Link to="/">Home</Link>
	  <Link to="hello">Hello World</Link>
	</nav>
	<div>
	  <Route path="hello" component="{HelloWorld}" name="world" />
	  <Route path="/" component="{Home}" name="home" />
	</div>
</Router>
