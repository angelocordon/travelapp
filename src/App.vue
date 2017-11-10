<template>
  <section id="app" class="hero is-dark is-fullheight">
    <nav-bar></nav-bar>
    <hero-body></hero-body>
    <hero-footer
      :background-owner="header.background.owner"
      :background-id="header.background.id">
    </hero-footer>
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
    },

    data: function () {
      return {
        header: {
          background: {
            id: '',
            owner: '',
            url: ''
          }
        }
      }
    },

    beforeMount: function () {
      this.header = {
        background: {
          id: 'ioy3bN5Irew',
          owner: 'Spencer Watson',
          url: 'photo-1504814532849-cff240bbc503?auto=format&fit=crop&w=1868&q=60&ixid=dW5zcGxhc2guY29tOzs7Ozs%3D'
        }
      }
    },

    mounted: function () {
      this.setHeaderBackground()
    },

    computed: {
      backgroundImageUrl: function () {
        return `url(https://images.unsplash.com/${this.header.background.url})`
      }
    },

    methods: {
      setHeaderBackground: function () {
        document.getElementById('app')
          .style
          .backgroundImage = this.backgroundImageUrl
      }
    }
  }
</script>

<style lang="scss" scoped>
  .hero {
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }
</style>
