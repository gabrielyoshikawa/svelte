<script>
  import Router from "svelte-spa-router";
  import Bindings from "./lib/Bindings.svelte";
  import ReactiveValues from "./lib/ReactiveValues.svelte";
  import Loops from "./lib/Loops.svelte";
  import HomePage from "./lib/HomePage.svelte";
  import InlineFunction from "./lib/InlineFunction.svelte";
</script>

<Router
  routes={{
    "/": HomePage,
    "/bindings": Bindings,
    "/reactive-values": ReactiveValues,
    "/loops": Loops,
    "/inline-function": InlineFunction,
  }}
/>

<style>
</style>
