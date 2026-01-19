<template>
  <div class= "Grapes>
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'GRAPES',
      message: 'I like Grapes'
    }
  }
};
</script>

<style>
  .Grapes {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: purple;
  }
</style>