<template>
  <div id="app">
    <h1>Agenda</h1>
    <FullCalendar :options='calendarOptions' />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import FullCalendar from '@fullcalendar/vue';
import dayGridPlugin from '@fullcalendar/daygrid';

@Component({
  components: {
    FullCalendar,
  },
  data: () => ({
    calendarOptions: {
      plugins: [dayGridPlugin],
      initialView: 'dayGridMonth',
      weekends: true,
      events: [
        { title: 'Meeting', start: new Date() },
      ],
    },
  }),
})

export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
