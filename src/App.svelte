<script>
  import Navbar from "./pages/Navbar.svelte";
  import Sidebar from "./pages/Sidebar.svelte";
  import Footer from "./pages/Footer.svelte";
  import Container from "./pages/Container.svelte";
  import Home from "./pages/Home.svelte";
</script>

<style>

</style>

<header class="header">
  <Navbar />
</header>

<div class="d-flex align-items-stretch">
  <Sidebar />
  <div class="page-holder w-100 d-flex flex-wrap">
    <!-- <Container /> -->
    <Home />
    <!-- Footer -->
    <Footer />
  </div>
</div>
