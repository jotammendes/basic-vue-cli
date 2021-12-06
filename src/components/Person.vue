<template>
  <h2>Essa é a descrição da pessoa: {{ name }}</h2>
  <Info :email="email" :is_working=false />
  <Form />
</template>

<script>
  import Info from './Info';
  import Form from './Form';

  export default {
    name: 'Person',
    components: {
      Info,
      Form
    },
    data() {
      return {
        name: 'Matheus',
        email: 'matheus2@email.com'
      }
    }
  }
</script>
