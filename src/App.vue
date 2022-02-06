<template>
  <div id="app">
    <b-navbar toggleable="sm">
      <b-navbar-brand>CodeTheorist</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/" exact exact-active-class="text-success"
            >Home</b-nav-item
          >
          <b-nav-item :to="{ name: 'About' }" active-class="text-success"
            >About</b-nav-item
          >
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <div style="min-height: calc(100vh - 6rem)">
      <router-view />
    </div>
    <b-nav class="justify-content-center">
      <b-nav-item
        v-if="false"
        :to="{ name: 'Contact' }"
        link-classes="text-dark"
        >Contact</b-nav-item
      >
    </b-nav>
  </div>
</template>

<style lang="scss">
@import "~@/assets/scss/vendors/bootstrap-vue/index";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
