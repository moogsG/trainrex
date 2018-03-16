<template>
  <b-navbar toggleable="md"  fixed="top" style="background-color: #F13E2F;">

    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

    <b-navbar-brand href="#"><img id="logo" src="../assets/logo.png" alt="BV" fluid> </b-navbar-brand>
    <b-collapse is-nav id="nav_collapse">
      <b-navbar-nav class="ml-auto" center>
        <b-nav-text class="logo-font" fluid scrolled>TrainRex</b-nav-text>
      </b-navbar-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav id="navbar-test" class="ml-auto" right>
        <b-nav-item href="#">Link</b-nav-item>
        <b-nav-item href="#">Disabled</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  name: 'Nav',
  data () {
    return {

    }
  },
  props: ['scrolled']
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Freckle+Face');
#logo {
   max-width:40px;
   max-height:40px;
   align-items: center;
}
.logo-font {
  font-size: 30px;
  font-family: 'Freckle Face', cursive;
}
.navbar {
  align-items: initial;
}

.navbar-collapse {
  align-items: initial !important;
}
.nav-item{
  align-items: initial !important;
}
#navbar-test{
  align-items: initial !important;
}
</style>
