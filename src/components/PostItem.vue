<template>
  <div class="post">
    <div>
      <h3>{{post.title}}</h3>
      <p>{{post.body}}</p>
    </div>
    <div class="post__buttons">
      <my-button class="btn--edit" @click="postEdit">Edit</my-button>
      <my-button class="btn--delete" @click="$emit('remove', post)">Delete</my-button>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      post: {
        type: Object,
        required: true
      }
    },
    methods: {
      postEdit(event) {
        
      },
      postDelete(event) {

      }
    }
  }
</script>

<style scoped>
  .post {
    max-width: 550px;
    padding: 15px;
    border: 1px solid black;
    margin: 15px 5px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
  }
  .post__buttons {
    align-self: flex-end;
    display: flex;
    justify-content: space-between;
  }
  .btn--delete {
    background: red;
  }
  .btn--delete:hover {
    background: rgb(170, 0, 0);
  }

</style>