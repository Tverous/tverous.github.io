<template>
  <article>
    <nuxt-content :document="page" />
  </article>
</template>

<script lang="ts">
export default {
  data() {
    return {
      page: {}
    }
  },
  async fetch() {
    this.page = await this.$content('home').fetch()
  }
}
</script>

<style lang="scss">
.nuxt-content {
  hr {
    margin-top: 1%;
    margin-bottom: 0%;
  }

  :is(h1, h2, h3, h4, h5) {
    margin-top: 2%;
    margin-bottom: 1%;
  }

  .note {
    display: table;
    width: 100%;
    .note-content {
      display: table-cell;
      vertical-align: middle;
      width: 70%;
      p {
        margin-top: 1%;
        margin-bottom: 1%;
      }
      ul {
        margin-top: 1%;
        li {
          margin-top: 1%;
        }
      }
    }
    .note-logo-bio {
      display: table-cell;
      vertical-align: middle;
      width: 30%;
      text-align: center;
      img {
        max-height: 15vw;
        border-radius: 10%;
      }
    }
    .note-logo {
      display: table-cell;
      vertical-align: middle;
      width: 30%;
      text-align: center;
      img {
        min-height: 4vw;
        max-height: 6vw;
        max-width: 15vw;
      }
    }
    .logo-content {
      p {
        display: inline-block;
      }
    }
  }
}
</style>
