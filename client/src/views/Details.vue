<template>
  <section class="section section-skew">
    <div class="container">
      <card shadow class="card-profile mt--250" no-body>
        <div class="px-4">
          <div class="row justify-content-center">
            <div class="col-lg-11 order-lg-1">
              <div class="card-profile-stats d-flex justify-content-between">
                <div>
                  <span class="heading">{{ movie.title }}</span>
                </div>

                <div>
                  <span class="description">
                    <i class="fa fa-map-marker"></i>
                    {{ movie.release_date }}</span
                  >
                </div>
              </div>
            </div>
          </div>

          <div class="row justify-content-center">
            <div class="col-lg-11 order-lg-1 text-center title">
              <h2>{{ movie.title }}</h2>

              <div class="h6 font-weight-300 mt-4">By {{ movie.author }}</div>

              <div style="font-size: 0.8rem">
                Published - {{ getDate(movie.release_date) }}
              </div>
            </div>
          </div>

          <div class="mt-5 py-5 border-top text-justify">
            <div class="row justify-content-center">
              <div
                class="col-lg-9 news"
                v-html="sanitize(movie.overview)"
              ></div>
            </div>
          </div>
        </div>
      </card>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "Details",
  components: {},
  props: {
    id: String, // received from $router.params
    movie: Object,
  },
});
</script>
