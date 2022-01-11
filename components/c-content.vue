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

<style>

.nuxt-content hr {
  margin-top: 1%;
  margin-bottom: 0%;
}

.nuxt-content .note {
  display: table;
  width: 100%;
}

.nuxt-content .note .note-content {
  display: table-cell;
  vertical-align: middle;
  width: 60%;
}

.nuxt-content .note .note-content :is(h1, h2, h3, h4, h5) {
  margin-top: 2%;
  margin-bottom: 1%;
}

.nuxt-content .note .note-content p {
  margin-top: 1%;
  margin-bottom: 1%;
}

.nuxt-content .note .note-content ul {
  margin-top: 1%;
}

.nuxt-content .note .note-content ul li{
  margin-top: 1%;
}

.nuxt-content .note .note-logo {
  display: table-cell;
  vertical-align: middle;
  width: 40%;
  text-align: center;
}

.nuxt-content .note .note-logo img {
  width: auto;
  height: 50%;
  max-height: 6vw;
}

.nuxt-content .note .logo-content p {
  display: inline-block;
  padding: 1%;
}

</style>
