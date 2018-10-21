<template>
  <nuxt-link :to="redirection">
    <div class="media">
      <img :src="actor.image" alt="Avatar" style="width: 100%">
    </div>
    <div class="card">
      <div>
        <h4><b>{{ actor.name }}</b>&nbsp;<em>({{ actor.age }})</em></h4>
      </div>
    </div>
  </nuxt-link>
</template>

<script>
  export default {
    props: {
      actor: {
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
    height: 15rem;
    width: 13rem;
    overflow: hidden;
    margin: auto;
  }

  .card {
    padding: .5rem;
  }
</style>
