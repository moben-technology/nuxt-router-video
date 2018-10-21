<template>
  <div class="container">
    <div class="card-container">
      <div class="card">
        <img :src="actor.image" alt="Avatar">
        <div class="biography">
          <h4><b>{{ actor.name }}</b>&nbsp;<em>({{ actor.age }})</em></h4><br/>
          <p>{{ actor.biography }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import ActorCard from "../actor/ActorCard";

  export default {
    components: {ActorCard},
    props: {
      actor: {
        type: Object,
        default: () => {
        }
      }
    }
  }
</script>

<style scoped>

  img {
    width: 13rem;
  }

  .biography {
    padding: 1rem 2rem;
  }

  .card {
    padding: 2rem 3rem 2rem 3rem;
    display: grid;
    grid-template-columns: auto auto;
  }

  .card-container {
    width: 70rem;
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
    margin: auto;
    display: grid;
    grid-template-columns: auto auto;
  }

</style>
