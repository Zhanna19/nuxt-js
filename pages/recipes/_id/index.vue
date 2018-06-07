<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img :src="recipe.thumbnail" alt="">
    </div>
    <p>{{ recipe.description }}</p>
  </section>
</template>

<script>
    export default {
      asyncData (context) {
        return new Promise(((resolve, reject) => {
          setTimeout(() => {
            resolve({
              recipe : [
                {
                  id: '1',
                  title: 'Donut',
                  previewText: 'Tasty donut',
                  description: 'mmmmmm',
                  thumbnail: 'http://ichef.bbci.co.uk/wwfeatures/wm/live/1280_720/images/live/p0/4s/6j/p04s6jkr.jpg'
                },
                {
                  id: '2',
                  title: 'Donut',
                  previewText: 'Tasty donut',
                  description: 'mmmmmm',
                  thumbnail: 'http://ichef.bbci.co.uk/wwfeatures/wm/live/1280_720/images/live/p0/4s/6j/p04s6jkr.jpg'
                },
                {
                  id: '3',
                  title: 'Donut',
                  previewText: 'Tasty donut',
                  description: 'mmmmmm',
                  thumbnail: 'http://ichef.bbci.co.uk/wwfeatures/wm/live/1280_720/images/live/p0/4s/6j/p04s6jkr.jpg'
                }
              ].find(el => el.id === context.params.id)
            })
          }, 1500)
        }))
      }
    }
</script>

<style scoped>
  .single-recipe {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-flow: column;
  }
  img {
    max-width: 50%;
  }
</style>
