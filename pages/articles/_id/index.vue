<template>
    <div>
      <h3>we are in article {{ article.title }}</h3>
      <nuxt-link :to="`${article.slug}/edit`"><button> Edit</button></nuxt-link>
    </div>
</template>

<script>
    export default {
      name: "_id",
      props: ['article']
    }
</script>

<style scoped>

</style>
