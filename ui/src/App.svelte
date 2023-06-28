<script>
  import Router from "svelte-spa-router";
  import Bindings from "./lib/Bindings.svelte";
  import ReactiveValues from "./lib/ReactiveValues.svelte";
</script>

<Router
  routes={{
    "/": Bindings,
    "/reactive-values": ReactiveValues,
  }}
/>

<style>

</style>
