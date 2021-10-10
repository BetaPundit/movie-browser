<template>
  <b-container class="py-4">

    <!-- Search bar -->
    <b-form inline>
      <b-form-input
        id="search"
        class="mb-2 mr-sm-2 mb-sm-0"
        placeholder="Movie Name"
      ></b-form-input>

      <b-button variant="primary">Search</b-button>
    </b-form>

    <!-- Movie list -->
    <b-section> 
      
    </b-section>
  </b-container>

</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'Home',
  components: {

  },
});
</script>

