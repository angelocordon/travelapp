<template>
  <div class="hero-body">
    <div class="container">
      <div class="columns">
        <div class="column is-three-fifths">
          <h1 class="title is-1 is-uppercase is-spaced">
            It's time to make your great escape.
          </h1>

          <p class="subtitle is-3">Where should we go?</p>

          <div class="field has-addons">
            <div class="control has-icons-left">
              <input class="input is-large"
                     type="text"
                     placeholder="Try Iceland.">
              <span class="icon is-large is-left">
                <i class="fa fa-compass"></i>
              </span>
            </div>
            <div class="control">
              <button class="button is-info is-large">
                <i class="fa fa-arrow-circle-o-right"></i>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'hero-body'
  }
</script>
