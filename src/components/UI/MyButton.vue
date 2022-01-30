<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script>
  export default {
    name: 'my-button'
  }
</script>

<style scoped>
  .btn {
    padding: 10px 30px;
    margin-right: 15px;
    border-radius: 4px;
    border: none;
    background: teal;
    color: white;
    font-size: 16px;
    transition: all .2s ease-in-out;
    cursor: pointer;
  }
  .btn:hover {
    background: rgb(0, 80, 80);
    transition: all .2s ease-in-out;
  }
</style>