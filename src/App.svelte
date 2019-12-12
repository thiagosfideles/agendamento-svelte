<script>
  import Navbar from "./pages/Navbar.svelte";
  import Sidebar from "./pages/Sidebar.svelte";
  import Container from "./Container.svelte";
  import menuOption from "./menu-store";
  import Footer from "./pages/Footer.svelte";

  let opcao = "";

  menuOption.subscribe(opc => {
    opcao = opc;
  });
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
    <Container content={opcao} />
    <!-- Footer -->
    <Footer />
  </div>
</div>
