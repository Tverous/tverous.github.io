<template>
  <table>
    <tbody>
      <tr>
        <td style="width: 60%">
          <div>
            <h5>
              {{ data }}
            </h5>
            <p v-for="desc in data.description" :key="desc.id">
              {{ desc }}
            </p>
          </div>
        </td>
        <td style="text-align: center">
          <img :src="data.logo" alt="logo" />
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script lang="ts">
export default {
  props: {
    table: {
      type: String,
      default: '',
    },
  },
  data() {
    return {
      data: {},
    };
  },
  async fetch() {
    this.data = await this.$content('about').only(this.table).fetch();
  },
};
</script>

<style scoped>
table {
  width: 100%;
}

table td img {
  width: 40%;
  height: auto;
}
</style>
