<template>
  <div class="app">
    <post-form
    @create="createPost"
    />
    <post-list
    :posts="posts"
    @remove="removePost"
    />
  </div>
</template>

<script>
import PostForm from "@/components/PostForm.vue";
import PostList from "@/components/PostList.vue";

export default {
  components: {
    PostForm, PostList
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'Post 1', body: 'lorem ipsum dolor sit amet consectetur'},
        {id: 2, title: 'Post 2', body: 'lorem ipsum dolor sit amet consectetur'},
        {id: 3, title: 'Post 3', body: 'lorem ipsum dolor sit amet consectetur'}
      ],
      title: '',
      body: ''
    }
  },
  methods: {
    createPost(post, second, third) {
      this.posts.push(post);
    },
    removePost(post) {
      this.posts = this.posts.filter(p => p.id !== post.id);
    }
  }
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
</style>