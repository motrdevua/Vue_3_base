<template>
  <div>
    <h3>Список постов</h3>
    <post-item
    v-for="post in posts"
    :key="post.id"
    :post="post"
    @remove="$emit('remove', post)"/>
  </div>
</template>

<script>
import PostItem from '@/components/PostItem.vue'
export default {
  components: { PostItem },
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
  h3 {
    font-size: 24px;
    margin: 15px 5px;
  }
</style>