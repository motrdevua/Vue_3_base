<template>
  <input type="text" class="input" @input="updateInput" :value="modelValue" aria-label="input">
</template>

<script>
  export default {
    name: 'my-input',
    props: {
      modelValue: [String, Number]
    },
    methods: {
      updateInput(event) {
        this.$emit('update:modelValue',  event.target.value)
      }
    }
  }
</script>

<style scoped>
  .input {
    padding: 10px 15px;
    margin: 0 15px 0 0;
  }
</style>