<template>
  <div>
    <h2>Meu formulário:</h2>
    <form @submit="submitForm">
      <div>
        <input type="text" v-model="name" />
      </div>
      <div>
        <input type="text" v-model="email" />
      </div>
      <Submit />
    </form>
  </div>
</template>

<script>
  import InputText from './form/InputText';
  import Submit from './form/Submit';

  export default {
    name: 'Form',
    components: {
      InputText,
      Submit
    },
    data() {
      return {
        name: '',
        email: ''
      }
    },
    methods: {
      submitForm(event) {
        event.preventDefault();

        const name = this.name;
        const email = this.email;

        console.log('Formulário enviado');
        console.log('o nome é: '+ name);
        console.log('o email é: '+ email);
      }
    }
  }
</script>

<style scoped>
  div {
    margin: 10px 0;
  }
</style>
