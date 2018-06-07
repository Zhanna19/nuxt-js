<template>
  <nuxt-link :to="'/recipes/' + id ">
    <article class="recipe">
      <div class="thumbnail" :style="'background-image: url('+ thumbnail + ')'"></div>
      <h1>{{ title }}</h1>
      <p>{{ previewText }}</p>
    </article>
  </nuxt-link>
</template>

<script>
    export default {
      name: 'Recipe',
      props: ['thumbnail', 'title', 'previewText', 'id']
    }
</script>

<style scoped>
  .recipe {
    box-sizing: border-box;
    width: 280px;
    padding: 8px;
    border: 1px solid #ccc;
    box-shadow: 0 2px 2px #eee;
  }
  .thumbnail {
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 200px;
  }
</style>
