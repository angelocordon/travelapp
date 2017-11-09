<template>
  <section id="app" class="hero is-primary is-fullheight">
    <div class="hero-head">
      <nav class="navbar">
        <div class="container">
          <div class="navbar-menu">
            <div class="navbar-brand">
              <a class="navbar-item">🜃</a>
            </div>
            <div class="navbar-end">
              <a class="navbar-item">☰</a>
            </div>
          </div>
        </div>
      </nav>
    </div>

    <div class="hero-body">
      <div class="container">
        <h1 class="title is-uppercase">
          It's time to make your great escape.
        </h1>
      </div>
    </div>

    <div class="hero-foot">
      <nav class="navbar">
        <div class="container">
          <div class="navbar-menu">
            <div class="navbar-end">
              <a href="https://github.com/angelocordon/travelapp" target="_new" class="navbar-item is-size-7"><i class="fa fa-code"></i> Coded with Vue + Bulma by Angelo Cordon.</a>
              <a href="https://dribbble.com/shots/3121830-Desktop-app-exploration-for-Traveling" target="_new" class="navbar-item is-size-7"><i class="fa fa-dribbble"></i> Inspiration from Andrew Baygulov.</a>
            </div>
          </div>
        </div>
      </nav>
    </div>
  </section>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang="scss">
  .navbar-brand > .navbar-item { font-size: 3rem; }

  .fa { margin-right: 0.5rem; }

  .hero {
    background-image: url('https://images.unsplash.com/photo-1455620611406-966ca6889d80?auto=format&fit=crop&w=2330&q=60&ixid=dW5zcGxhc2guY29tOzs7Ozs%3D');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }
</style>
