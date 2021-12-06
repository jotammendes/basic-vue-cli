<template>
  <div>
    <p v-if="is_working">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades.</p>

    <p>Utilizo as seguintes tecnologias para back-end:</p>
    <ul>
      <li v-for="(technology, index) in backend_technologies" :key="index">{{ technology }}</li>
    </ul>

    <p>Utilizo as seguintes tecnologias para front-end:</p>
    <ul>
      <li v-for="technology in frontend_technologies" :key="technology.id">{{ technology.language }}</li>
    </ul>

    <div>
      <button @click="showEmail">{{ button_text }}</button>
    </div>

    <p v-show="show_email">Mande uma mensagem para: {{ email }}</p>
    <p class="portfolio">Para acessar meu portfólio <a v-bind:href="link" target="_blank">basta clicar aqui</a></p>
    <Picture />
  </div>
</template>

<script>
  import Picture from './Picture';
 
  export default {
    name: 'Info',
    components: {
      Picture
    },
    props: {
      email: String,
      is_working: Boolean
    },
    data() {
      return {
        show_email: true,
        link: 'https://google.com',
        button_text: 'Esconder e-mail',
        backend_technologies: ['JavaScript', 'PHP', 'Python', 'Ruby'],
        frontend_technologies: [
          {id: 1, language: 'HTML'},
          {id: 2, language: 'CSS'},
          {id: 3, language: 'Vue'}
        ]
      }
    },
    methods: {
      showEmail() {
        this.show_email = !this.show_email;
        if(!this.show_email) {
          this.button_text = 'Mostrar e-mail';
        } else {
          this.button_text = 'Esconder e-mail';
        }
      }
    }
  }
</script>

<style>
  .paragraph-father {
    color: red;
  }
</style>
