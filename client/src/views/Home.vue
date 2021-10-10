<template>
  <section class="section section-lg">
    <!-- Search bar -->
    <div class="container" style="margin-top: 2rem">
      <b-form inline>
        <b-form-input
          id="search"
          class="mb-2 mr-sm-2 mb-sm-0"
          placeholder="Movie Name"
        ></b-form-input>

        <b-button variant="primary">Search</b-button>
      </b-form>
    </div>

    <!-- Movie list -->
    <section class="section section-lg">
      <div class="container" style="margin-top: 6rem">
        <div class="row">
          <movie-card
            v-for="movie in movies"
            :key="movie.id"
            :movie="movie"
          ></movie-card>
        </div>
      </div>
    </section>
  </section>
</template>

<script lang="ts">
import Vue from "vue";
import MovieCard from "../components/MovieCard.vue";
import gql from "graphql-tag";

export default Vue.extend({
  name: "Home",
  components: {
    MovieCard,
  },
  apollo: {
    movies: gql`
      query {
        movies {
          id
          title
          overview
          popularity
          genre_ids
          adult
          release_date
        }
      }
    `,
  },
});
</script>
