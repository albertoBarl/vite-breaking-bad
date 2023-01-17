<template lang="">
  <resultsMess />
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
import resultsMess from "./singleElements/resultsMess.vue";
import { store } from "../assets/datas/store.js";

export default {
  components: {
    appCard,
    resultsMess,
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
