<template>
  <section id="app" class="hero is-dark is-fullheight">
    <nav-bar></nav-bar>
    <hero-body></hero-body>
    <hero-footer></hero-footer>
  </section>
</template>

<script>
  import NavBar from './components/NavBar'
  import HeroBody from './components/HeroBody'
  import HeroFooter from './components/HeroFooter'

  export default {
    name: 'app',
    components: {
      NavBar,
      HeroBody,
      HeroFooter
    }
  }
</script>

<style lang="scss" scoped>
  .fa { margin-right: 0.5rem; }

  .hero {
    background-image: url('https://images.unsplash.com/photo-1437846972679-9e6e537be46e?auto=format&fit=crop&w=2551&q=60&ixid=dW5zcGxhc2guY29tOzs7Ozs%3D');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }
</style>
