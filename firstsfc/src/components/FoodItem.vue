<template>
  <div class="strawberries">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'strawberries',
      message: 'I like like strawberries'
    }
  }
};
</script>

<style>
  .strawberries {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: pink;
  }
</style>