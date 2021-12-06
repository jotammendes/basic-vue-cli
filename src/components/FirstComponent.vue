<template>
  <div>
    <Reuse />
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ name }} e trabalho como {{ occupation }}</p>

    <Reuse />
    <MultiplesEvents />
    <Reuse />
    <Reuse />
    <Reuse />
  </div>
</template>

<script>
  import MultiplesEvents from './MultiplesEvents';
  import Reuse from './Reuse';

  export default {
    name: 'FirstComponent',
    components: {
      MultiplesEvents,
      Reuse
    },
    data() {
      return {
        name: 'Matheus',
        occupation: 'programador'
      }
    }
  }
</script>
