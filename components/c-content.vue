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

.nuxt-content table {
  width: 100%;
  margin-bottom: 1%;
}

.nuxt-content table p {
  line-height: 1.5;
}

.nuxt-content table td:nth-child(1) {
  width: 60%;
}

.nuxt-content table td:nth-child(2) {
  text-align: center;
}

.nuxt-content table td img {
  width: 50%;
  height: auto;
}
</style>
