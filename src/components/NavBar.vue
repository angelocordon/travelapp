<template>
  <div class="hero-head">
    <nav class="navbar">
      <div class="container">
        <div class="navbar-menu">
          <div class="navbar-brand">
            <a class="navbar-item"
               @click="clearQuery">
              🜃
            </a>
          </div>
          <div class="navbar-end">
            <a class="navbar-item">
              <i class="fa fa-shopping-cart"></i>
            </a>
            <a class="navbar-item">
              <i class="fa fa-info-circle"></i>
            </a>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {
    name: 'nav-bar',

    methods: {
      clearQuery: function () {
        this.$emit('clear')
      }
    }
  }
</script>

<style lang="scss" scoped>
  .navbar-brand > .navbar-item { font-size: 3rem; }
</style>
