<template>
  <div class="body">
    <h1>Prochaines sorties au cinéma</h1>
    <movie-list :movies="movies"></movie-list>
  </div>
</template>
<script>
  import MovieList from "../../components/movie/MovieList";
  import data from "../../data/movies.json"

  export default {
    components: {MovieList},
    data() {
      return {
        movies: data
      }
    }
  }
</script>
