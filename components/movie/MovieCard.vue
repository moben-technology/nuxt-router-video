<template>
    <nuxt-link :to="redirection">
      <div class="media">
        <img :src="movie.image" alt="Avatar" style="width: 100%">
      </div>
      <div class="card">
        <div>
          <h4><b>{{ movie.title }}</b>&nbsp;<em>({{ movie.year }})</em></h4>
          <p>{{ movie.description }}</p>
        </div>
      </div>
    </nuxt-link>
</template>

<script>
  export default {
    props: {
      movie: {
        type: Object,
        default: () => {}
      },
      redirection: {
        type: String,
        default: () => ''
      }
    }
  }
</script>

<style scoped>
  .media {
    height: 20rem;
    overflow: hidden;
  }

  .card {
    padding: .5rem;
  }
</style>
