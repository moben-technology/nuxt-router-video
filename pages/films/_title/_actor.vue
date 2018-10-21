<template>
  <div class="body">
    <actor-detail :actor="actor"></actor-detail>
  </div>
</template>
<script>
  import ActorDetail from "../../../components/actor/ActorDetail";
  import data from "../../../data/movies.json"

  export default {
    components: {ActorDetail},
    asyncData({ params }) {
      return {
        actor: data.find(movie => movie.id === params.title).casting.find(actor => actor.id === params.actor)
      }
    }
  }
</script>
