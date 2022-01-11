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
  width: 100%;
  overflow: hidden;
  position: relative;
  border: solid 1px #ff0000;
}

.nuxt-content .note .note-content {
  width: 70%;
  display: inline-block;
  border: solid 1px #000;
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
  width: 30%;
  text-align: center;
  border: solid 1px #000;
  height: 100%;
  position: absolute;
  right: 0;
  top: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.nuxt-content .note .note-logo img {
  width: 50%;
}

</style>
