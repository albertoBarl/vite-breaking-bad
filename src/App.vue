<template lang="">
  <div v-if="store.isLoaded">
    <AppHeader />
    <appDeck @filter="getCards" class="ms-5 mt-5" />
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
import appDeck from "./components/singleElements/appDeck.vue";

import axios from "axios";
import { store } from "./assets/datas/store.js";

export default {
  components: {
    appDeck,
    AppContent,
    AppHeader,
    Loader,
    appDeck,
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
      let myUrl = `${store.url}${store.selectedGen}`;
      axios.get(myUrl).then((response) => {
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
