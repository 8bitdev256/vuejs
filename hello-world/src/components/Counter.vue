<template>
    <div>
        <button v-on:click="decrement">-</button>
        {{ count }}
        <button v-on:click="increment">+</button>
    </div>
</template>

<script>
import Vue from 'vue';
import Component from 'vue-class-component';

@Component
export default class Counter extends Vue {
    count = 0

    decrement() {
      this.count -= 1;
    }

    increment() {
      this.count += 1;
    }
}
</script>
