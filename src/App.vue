<template>
  <div id="app">
    <b-navbar>
      <b-navbar-brand>CodeTheorist</b-navbar-brand>
      <b-navbar-nav>
        <b-nav-item to="/" exact exact-active-class="text-success"
          >Home</b-nav-item
        >
        <b-nav-item :to="{ name: 'About' }" active-class="text-success"
          >About</b-nav-item
        >
      </b-navbar-nav>
    </b-navbar>
    <div style="min-height: calc(100vh - 6rem)">
      <router-view />
    </div>
    <b-nav align="center">
      <b-nav-item :to="{ name: 'Tos' }">Terms of Service</b-nav-item>
      <b-nav-item :to="{ name: 'PrivacyPolicy' }">Privacy Policy</b-nav-item>
      <b-nav-item :to="{ name: 'Contact' }">Contact</b-nav-item>
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
