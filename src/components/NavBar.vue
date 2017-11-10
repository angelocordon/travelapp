<template>
  <div class="hero-head">
    <nav class="navbar">
      <div class="container">
        <div class="navbar-menu">
          <div class="navbar-brand">
            <a class="navbar-item">🜃</a>
          </div>
          <div class="navbar-end">
            <a class="navbar-item">
              <i class="fa fa-shopping-cart"></i>
            </a>
            <a class="navbar-item">☰</a>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {
    name: 'nav-bar'
  }
</script>

<style lang="scss" scoped>
  .navbar-brand > .navbar-item { font-size: 3rem; }
</style>
