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
      <a href="." class="sidebar-link text-muted">
        <i class="o-survey-1 mr-3 text-gray" />
        <span>Forms</span>
      </a>
    </li>
    <li class="sidebar-list-item">
      <a
        href="."
        data-toggle="collapse"
        data-target="#pages"
        aria-expanded="false"
        aria-controls="pages"
        class="sidebar-link text-muted">
        <i class="o-wireframe-1 mr-3 text-gray" />
        <span>Pages</span>
      </a>
      <div id="pages" class="collapse">
        <ul
          class="sidebar-menu list-unstyled border-left border-primary
          border-thick">
          <li class="sidebar-list-item">
            <a href="." class="sidebar-link text-muted pl-lg-5">Page one</a>
          </li>
          <li class="sidebar-list-item">
            <a href="." class="sidebar-link text-muted pl-lg-5">Page two</a>
          </li>
          <li class="sidebar-list-item">
            <a href="." class="sidebar-link text-muted pl-lg-5">Page three</a>
          </li>
          <li class="sidebar-list-item">
            <a href="." class="sidebar-link text-muted pl-lg-5">Page four</a>
          </li>
        </ul>
      </div>
    </li>
    <li class="sidebar-list-item">
      <a href="." class="sidebar-link text-muted">
        <i class="o-exit-1 mr-3 text-gray" />
        <span>Login</span>
      </a>
    </li>
  </ul>
</div>
