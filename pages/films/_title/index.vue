

<template>
  <div class="body">
    <movie-detail :movie="movie" ></movie-detail>
  </div>
</template>

<script>
  import MovieDetail from "../../../components/movie/MovieDetail";
  import data from "../../../data/movies.json"

  export default {
    components: {MovieDetail},
    asyncData(context) {
      return {
        movie: data.find(movie => movie.id === context.params.title)
      }
    }
  }
</script>


