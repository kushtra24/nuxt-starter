<template>
    <div>
      <h1>Articles works</h1>
      <div v-for="article in articles" :key="article.id">
        <nuxt-link :to="`/articles/${article.slug}`">{{ article.title }}</nuxt-link>
      </div>
    </div>
</template>

<script>
    export default {
        name: "articles",
      async asyncData(context) {
          let response = await context.$axios.get('/articles');
          let articles = response.data;
          return {
            articles
          }
      }
    }
</script>
