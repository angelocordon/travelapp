<template>
  <div class="hero-body">
    <div class="container">
      <div class="columns">
        <div class="column is-three-fifths">
          <h1 class="title is-1 is-uppercase is-spaced"
              :class="activeQueryClass">
            It's time to make your great escape.
          </h1>

          <p class="subtitle is-3"
             :class="activeQueryClass">
            Where should we go?
          </p>

          <div class="field has-addons">
            <div class="control has-icons-left">
              <input class="input is-large"
                     type="text"
                     placeholder="Try Iceland."
                     v-model="destination"
                     @keyup.enter="searchDestination">
              <span class="icon is-large is-left">
                <i class="fa fa-compass"></i>
              </span>
            </div>
            <div class="control">
              <button class="button is-info is-large"
                      @click="searchDestination">
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
    name: 'hero-body',

    props: {
      activeQuery: {
        type: Boolean,
        required: true
      }
    },

    data: function () {
      return {
        destination: ''
      }
    },

    computed: {
      activeQueryClass: function () {
        if (this.activeQuery) { return 'is-hidden' }
      }
    },

    watch: {
      destination: function () {
        if (!this.destination) { this.$emit('clear') }
      }
    },

    methods: {
      searchDestination: function () {
        if (this.destination) {
          this.$emit('query')
        }
      }
    }
  }
</script>

<style lang="scss" scoped>
  .input { text-transform: capitalize; }

  .is-hidden { display: none; }
</style>
