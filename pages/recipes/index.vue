<template>
  <section class="recipes">
      <Recipe
        v-for="recipe in recipes"
        :key="recipe.id"
        :title="recipe.title"
        :previewText="recipe.previewText"
        :thumbnail="recipe.thumbnail"
        :id="recipe.id"
      ></Recipe>
  </section>
</template>

<script>
  import Recipe from "../../components/Recipe";
  export default {
    components: {Recipe},
    asyncData () {
      return new Promise(((resolve, reject) => {
        setTimeout(() => {
          resolve({
            recipes : [
              {
                id: '1',
                title: 'Donut',
                previewText: 'Tasty donut',
                thumbnail: 'http://ichef.bbci.co.uk/wwfeatures/wm/live/1280_720/images/live/p0/4s/6j/p04s6jkr.jpg'
              },
              {
                id: '2',
                title: 'Donut',
                previewText: 'Tasty donut',
                thumbnail: 'http://ichef.bbci.co.uk/wwfeatures/wm/live/1280_720/images/live/p0/4s/6j/p04s6jkr.jpg'
              },
              {
                id: '3',
                title: 'Donut',
                previewText: 'Tasty donut',
                thumbnail: 'http://ichef.bbci.co.uk/wwfeatures/wm/live/1280_720/images/live/p0/4s/6j/p04s6jkr.jpg'
              }
            ]
          })
        }, 1500)
      }))
    }
  }
</script>

<style scoped>
  a {
    text-decoration: none;
  }
  .recipes {
    display: flex;
    flex-flow: row wrap;
    justify-items: center;
    align-items: center;
  }
</style>
