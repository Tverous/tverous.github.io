<template>
  <article>
    <nuxt-content :document="page" />
  </article>
</template>

<script>
export default {
  data() {
    return {
      page: {},
    };
  },
  async fetch() {
    this.page = await this.$content('home').fetch();
  },
};
</script>

// TODO: scoped style
<style>
.nuxt-content hr {
  margin-top: 1%;
}
</style>
