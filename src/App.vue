<template lang="">
  <div v-if="store.isLoaded">
    <AppHeader />
    <div class="p-5">
      <AppContent />
    </div>
  </div>
  <div v-else>
    <loader />
  </div>
</template>
<script>
import AppContent from "./components/AppContent.vue";
import AppHeader from "./components/AppHeader.vue";
import Loader from "./components/singleElements/loader.vue";
import axios from "axios";
import { store } from "./assets/datas/store.js";

export default {
  components: {
    AppContent,
    AppHeader,
    Loader,
  },
  data() {
    return {
      store,
    };
  },
  created() {
    this.getCards();
  },
  methods: {
    getCards() {
      axios.get(store.url).then((response) => {
        store.cardList = response.data.data;
        setTimeout(() => {
          store.isLoaded = true;
        }, 2000);
      });
    },
  },
};
</script>
<style lang="scss"></style>
