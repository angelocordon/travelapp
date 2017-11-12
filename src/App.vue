<template>
  <section id="app" class="hero is-dark is-fullheight">
    <hero-highlight-image :background-url="header.background.url"/>
    <nav-bar v-on:clear="clearQuery"/>
    <hero-body :active-query="activeQuery"
               v-on:query="activateQuery"
               v-on:clear="clearQuery"/>
    <hero-footer
      :background-owner="header.background.owner"
      :background-id="header.background.id"/>
  </section>
</template>

<script>
  import NavBar from './components/NavBar'
  import HeroHighlightImage from './components/HeroHighlightImage'
  import HeroBody from './components/HeroBody'
  import HeroFooter from './components/HeroFooter'

  export default {
    name: 'app',

    components: {
      NavBar,
      HeroHighlightImage,
      HeroBody,
      HeroFooter
    },

    data: function () {
      return {
        activeQuery: false,

        header: {
          background: {
            id: '',
            owner: '',
            url: ''
          }
        },

        featured: {
          background: {
            id: 'ioy3bN5Irew',
            owner: 'Spencer Watson',
            url: 'photo-1504814532849-cff240bbc503?auto=format&fit=crop&w=1868&q=60&ixid=dW5zcGxhc2guY29tOzs7Ozs%3D'
          }
        }
      }
    },

    mounted: function () {
      this.setFeaturedBackground()
    },

    computed: {

    },

    methods: {
      setFeaturedBackground: function () {
        this.header.background = this.featured.background
      },

      activateQuery: function () {
        this.activeQuery = true
      },

      clearQuery: function () {
        this.activeQuery = false
      }
    }
  }
</script>
