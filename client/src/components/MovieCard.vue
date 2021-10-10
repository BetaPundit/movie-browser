<template>
  <div class="col-sm-6 col-md-6 col-lg-4 mb-4 d-flex justify-content-center">
    <b-card
      :title="movie.title"
      :sub-title="'released on: ' + movie.release_date"
    >
      <b-card-text>
        {{ movie.overview }}
      </b-card-text>
      <a @click="route" class="card-link" style="cursor: pointer;">Read more</a>
    </b-card>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "MovieCard",
  components: {},
  props: {
    movie: Object,
  },
  methods: {
    route() {
      this.$router.push({
        name: "Details",
        // path: this.movie.id,
        params: { id: this.movie.id, movie: this.movie },
      });
    },
  },
});
</script>

<style scoped></style>
