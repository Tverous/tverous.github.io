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

.nuxt-content .note {
  color: red;
}

.nuxt-content .note .note-content {
  width: 70%;
  height: auto;
}

.nuxt-content .note .note-logo {
  width: 30%;
  height: auto;
  text-align: center;
  float: right;
}

.nuxt-content .note-logo img {
  width: 60%;
  height: auto;
}
</style>
