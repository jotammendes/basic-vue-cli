<template>
  <Header :is_logged="true" />
  <FirstComponent />
  <p class="paragraph-father">Testando</p>
  <LifeCycle />
  <Person />
</template>

<script>
import Header from './components/Header';
  import FirstComponent from './components/FirstComponent';
  import LifeCycle from './components/LifeCycle';
  import Person from './components/Person';

  export default {
    name: 'App',
    components: {
      Header,
      FirstComponent,
      LifeCycle,
      Person
    }
  }
</script>

<style>
  body {
    background-color: #333;
    color: #fff;
  }

  a {
    color: red;
  }

  .portfolio {
    background-color: #000;
  }
</style>
