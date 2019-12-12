<script>
  export let content;
  import Home from "./pages/Home.svelte";
  import Calendar from "./pages/Calendar.svelte";
</script>

<style>

</style>

{#if content === 'home'}
  <Home />
{:else if content === 'calendar'}
  <Calendar />
{/if}
