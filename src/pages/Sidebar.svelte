<script>
  import menuOption from "../menu-store";

  export let selected_option = "home";
  $: menu_opt = selected_option;

  function handleMenu(e) {
    e.preventDefault();
    selected_option = e.target.id;
    menuOption.set(selected_option);
  }
</script>

<style>

</style>

<div id="sidebar" class="sidebar py-3">
  <div
    class="text-gray-400 text-uppercase px-3 px-lg-4 py-4 font-weight-bold small
    headings-font-family">
    MAIN
  </div>
  <ul class="sidebar-menu list-unstyled">
    <li class="sidebar-list-item">
      <a
        class="sidebar-link text-muted"
        href="home"
        on:click={handleMenu}
        id="home">
        <i class="o-home-1 mr-3 text-gray" />
        <span>Home</span>
      </a>
    </li>

    <li class="sidebar-list-item">
      <a
        class="sidebar-link text-muted"
        href="calendar"
        on:click={handleMenu}
        id="calendar">
        <i class="o-table-content-1 mr-3 text-gray" />
        <span>Agendamento</span>
      </a>
    </li>
    <li class="sidebar-list-item">
      <a
        href="config"
        on:click={handleMenu}
        id="config"
        class="sidebar-link text-muted">
        <i class="o-settings-window-1 mr-3 text-gray" />
        <span>Administração</span>
      </a>
    </li>
    <li class="sidebar-list-item">
      <a
        href="dashboard"
        on:click={handleMenu}
        id="dashboard"
        class="sidebar-link text-muted">
        <i class="o-sales-up-1 mr-3 text-gray" />
        <span>Dashboard</span>
      </a>
    </li>
  </ul>
</div>
