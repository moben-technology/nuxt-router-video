<template>
  <div class="container">
    <div class="card-container">
      <div class="media">
        <img :src="movie.cover" alt="Avatar" style="width: 100%">
      </div>
      <div class="card">
        <div>
          <h4><b>{{ movie.title }}</b>&nbsp;<em>({{ movie.year }})</em></h4>
          <p>{{ movie.description }}</p>
          <div class="container">
            <h4>Casting</h4>
            <section class="actors">
              <div v-for="actor in movie.casting" :key="actor.id" class="actor">
                <actor-card :actor="actor" :redirection="`/films/${movie.id}/${actor.id}`"></actor-card>
              </div>
            </section>
          </div>
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
      movie: {
        type: Object,
        default: () => {
        }
      }
    }
  }
</script>

<style scoped>
  .media {
    height: 30rem;
    overflow: hidden;
  }

  .card {
    padding: 1rem 3rem 2rem 3rem;
  }

  .card-container {
    width: 60rem;
    height: 65rem;
    margin: auto;
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
  }

  .actors {
    display: grid;
    flex-direction: row;
    grid-gap: .5rem;
    grid-template-columns: auto auto auto;
    margin-top: 2rem;
    padding-left: 2.5rem;
  }

  .actor {
    margin: auto;
    cursor: pointer;
    text-align: center;
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
  }

  .actor:hover {
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.5);
  }

</style>
