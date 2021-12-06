<template>
  <div>
    <img :src="avatar" :alt="description">
    <ChangeImage @change-image="changeImage" />
  </div>
</template>

<script>
  import ChangeImage from './ChangeImage';

  export default {
    name: 'Picture',
    components: {
      ChangeImage
    },
    data() {
      return {
        avatar: '/img/avatar.png',
        description: 'Avatar'
      }
    },
    methods: {
      changeImage() {
        this.avatar = '/img/avatar2.png';
      }
    }
  }
</script>
