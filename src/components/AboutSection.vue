<template>
  <div class="row justify-center default-margin-top" v-if="showBanner">
  </div>
  <div v-if="showDescription" class="row justify-center default-margin-top">
    <AppDescription />
  </div>
  <div class="row justify-center default-margin-top">
  </div>
  <div class="row justify-center">
    <p>
      Built with
      <a href="https://quasar.dev" target="_blank" class="text-accent"
        >Quasar</a
      >
      and
      <a href="https://vuejs.org/" target="_blank" class="text-accent"
        >Vue.js</a
      >
    </p>
  </div>
  <div class="row justify-center">
    <p>
      Data provided by
      <a
        href="https://https://imdb-api.com/"
        target="_blank"
        class="text-accent"
        >IMDB</a
      >
    </p>
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue';
import AppDescription from './AppDescription.vue';
// import appConfig from 'src/appConfig';

export default defineComponent({
  name: 'AboutSection',
  components: { AppDescription },
  props: {
    showBanner: {
      type: Boolean,
      required: false,
      default: true,
    },
    showDescription: {
      type: Boolean,
      required: false,
      default: true,
    },
    numberOfItems: {
      type: Number,
      required: false,
    },
  },
});
</script>
