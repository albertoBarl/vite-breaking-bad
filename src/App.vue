<script>
import AppContent from "./components/AppContent.vue";
import axios from "axios";
import { store } from "./assets/datas/store.js";

export default {
  components: {
    AppContent,
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
<template lang="">
  <div>
    <AppContent />
  </div>
</template>
<style lang="scss"></style>
