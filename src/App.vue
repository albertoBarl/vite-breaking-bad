<template lang="">
  <AppHeader />
  <div class="p-5">
    <AppContent />
  </div>
</template>
<script>
import AppContent from "./components/AppContent.vue";
import AppHeader from "./components/AppHeader.vue";
import axios from "axios";
import { store } from "./assets/datas/store.js";

export default {
  components: {
    AppContent,
    AppHeader,
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
      });
    },
  },
};
</script>
<style lang="scss"></style>
