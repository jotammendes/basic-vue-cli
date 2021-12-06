<template>
  <div>
    <button @click="first(txt1, $event), second(txt2, $event), third(txt3, $event)">Ativar múltiplos eventos</button>
    <p>{{ multiples_events }}</p>
  </div>
</template>

<script>
  export default {
    name: 'MultiplesEvents',
    data() {
      return {
        multiples_events: "",
        txt1: "Primeiro evento!",
        txt2: "Segundo evento!",
        txt3: "Terceiro evento!"
      }
    },
    methods: {
      first(txt, event) {
        this.multiples_events = txt;
      },
      second(txt, event) {
        setTimeout(() => this.multiples_events = txt, 1000);
      },
      third(txt, event) {
        setTimeout(() => this.multiples_events = txt, 2000);
      }
    }
  }
</script>

<style scoped>
  div {
    margin: 100px;
  }
</style>
