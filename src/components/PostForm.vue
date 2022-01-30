<template>
  <form class="form" @submit.prevent>
    <h4 class="form-title">Создание поста</h4>

    <my-input 
    v-model="post.title" 
    placeholder="Название поста"/>
    <my-input 
    v-model="post.body" 
    placeholder="Текст поста"/>

    <my-button
    @click="createPost">
    Создать пост
    </my-button>
  </form>
</template>

<script>
  export default {
    data() {
      return {
        post: {
          title: '',
          body: ''
        }
      }
    },
    methods: {
      createPost() {
        if (this.post.title !== '' || this.post.body !== '') {
          this.post.id = Date.now();
          this.$emit('create', this.post)
          this.post = {
            title: '',
            body: ''
          }
        }
      }
    }
  }
</script>

<style scoped>
  .form {
    margin: 5px;
  }

  .form-title {
    font-size: 24px;
    margin: 15px 0;
  }
</style>