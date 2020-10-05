<template>
    <div>
      <nuxt-child :article="articles"></nuxt-child>
    </div>
</template>

<script>
    export default {
        name: "_id",
      async asyncData(context) {
        let response = await context.$axios.get(`/articles/${context.params.id}`);
        let articles = response.data;
        return {
          articles
        }
      }
    }
</script>

<style scoped>

</style>
