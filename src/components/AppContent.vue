<template lang="">
  <appDeck class="mb-3" />
  <div
    class="bg-body rounded container d-flex justify-content-center gap-5 p-5 flex-wrap"
  >
    <appCard
      v-for="(elem, index) in store.cardList"
      :key="index"
      :monster="elem"
    />
  </div>
</template>
<script>
import appCard from "./singleElements/appCard.vue";
import appDeck from "./singleElements/appDeck.vue";
import { store } from "../assets/datas/store.js";

export default {
  components: {
    appCard,
    appDeck,
  },
  data() {
    return {
      store,
    };
  },
};
</script>
<style lang="scss" scoped>
div.container {
  height: 76vh;
  overflow: auto;
}
</style>
