<script>
  import FullCalendar from "svelte-fullcalendar";
  import dayGridPlugin from "@fullcalendar/daygrid";
</script>

<style>

</style>

<div class="container-fluid px-xl-5">
  <section class="py-5">
    <div class="col mb-1 mx-auto">
      <div class="card">
        <div class="card-header">
          <h6 class="text-uppercase mb-0">Agendamento de aulas</h6>
        </div>
        <div class="card-body">
          <FullCalendar
            defaultView="dayGridMonth"
            plugins="{[dayGridPlugin]}"
            events={[{ title: 'event 1', date: '2019-12-15' }, { title: 'event 2', date: '2019-12-12' }]} />
        </div>
      </div>
    </div>
  </section>
</div>
