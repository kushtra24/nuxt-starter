<template>
<div>
  <h3>Editing {{ article.title }}</h3>
  <nuxt-link :to="`/articles/${article.slug}`"><button>back to article</button></nuxt-link>
</div>
</template>

<script>
    export default {
        name: "edit",
        props: ['article']
    }
</script>

<style scoped>

</style>
