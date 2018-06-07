<template>
    <header>
      <nav>
        <ul>
          <li><nuxt-link to="/">Start Page</nuxt-link></li>
          <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
          <li><nuxt-link to="/about">About</nuxt-link></li>
        </ul>
      </nav>
    </header>
</template>

<script>
    export default {
        name: 'Header'
    }
</script>

<style scoped>
  header {
    width: 100%;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-items: center;
    align-items: center;
  }

  li {
    margin: 0 10px;
  }

  a {
    text-decoration: none;
  }
</style>
