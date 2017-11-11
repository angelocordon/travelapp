<template>
  <div class="hero-foot">
    <nav class="navbar">
      <div class="container">
        <div class="navbar-menu">
          <div class="navbar-end">
            <a :href="attributionLink"
               target="_new"
               class="navbar-item is-size-7">
               <i class="fa fa-camera"></i> {{ attribution }}
            </a>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {
    name: 'hero-footer',

    props: {
      backgroundOwner: {
        type: String,
        required: true
      },

      backgroundId: {
        type: String,
        required: true
      }
    },

    computed: {
      attribution: function () {
        return `Image by ${this.backgroundOwner}`
      },

      attributionLink: function () {
        return `https://unsplash.com/photos/${this.backgroundId}`
      }
    }
  }
</script>

<style lang="scss" scoped>
  .fa { margin-right: 0.5rem; }
</style>
