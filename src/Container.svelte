<script>
  export let content;
  import Home from "./pages/Home.svelte";
  import Calendar from "./pages/Calendar.svelte";
  import Config from "./pages/Config.svelte";
  import Dashboard from "./pages/Dashboard.svelte";
</script>

<style>

</style>

{#if content === 'home'}
  <Home />
{:else if content === 'calendar'}
  <Calendar />
{:else if content === 'config'}
  <Config />
{:else if content === 'dashboard'}
  <Dashboard />
{/if}
