<template>
  <div class="hero-highlight-image"
       :style="{ background: backgroundImageUrl }">
  </div>
</template>

<script>
  export default {
    name: 'hero-highlight-image',

    props: {
      backgroundUrl: {
        type: String,
        required: false
      }
    },

    computed: {
      backgroundImageUrl: function () {
        return `url(https://images.unsplash.com/${this.backgroundUrl})`
      }
    }
  }
</script>

<style lang="scss" scoped>
  .hero-highlight-image {
    position: absolute;
    width: 100vw;
    height: 100vh;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }
</style>
