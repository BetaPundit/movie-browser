<template>
  <div px-2 py-2>
    <b-card :title=title :sub-title=release_date>
        <b-card-text>
        {{ overview }}
        </b-card-text>
        <a href="#" class="card-link">Read more</a>
    </b-card>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'MovieCard',
  components: {

  },
  props: {
    id: String,
    title: String,
    overview: String,
    popularity: Number,
    release_date: String
  }
});
</script>


<style scoped>

</style>