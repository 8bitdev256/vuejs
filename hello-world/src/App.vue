<template>
  <div id="app">
    <HelloWorld msg="Agenda"/>
    <Counter/>
    <FullCalendar :options='calendarOptions' />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import FullCalendar from '@fullcalendar/vue';
import dayGridPlugin from '@fullcalendar/daygrid';
import HelloWorld from './components/HelloWorld.vue';
import Counter from './components/Counter.vue';

@Component({
  components: {
    HelloWorld,
    Counter,
    FullCalendar,
  },
  data: () => ({
    calendarOptions: {
      plugins: [dayGridPlugin],
      initialView: 'dayGridMonth',
      weekends: false,
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
