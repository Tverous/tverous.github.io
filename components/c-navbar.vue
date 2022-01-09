<template>
  <div id="top-navbar">
    <b-navbar toggleable="lg" type="light">
      <b-navbar-brand brand href="/">Simon Tang</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav align="center">
          <b-nav-item href="#experience">Experiences</b-nav-item>
          <b-nav-item href="#publications">Publications</b-nav-item>
          <b-nav-item href="#honors">Honors</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<style scoped>
#top-navbar {
  background-color: white;
  border-bottom: 1px solid;
}
</style>
