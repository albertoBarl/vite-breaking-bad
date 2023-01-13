<script>
import appCard from "./singleElements/appCard.vue";
import { store } from "../assets/datas/store.js";

export default {
  components: {
    appCard,
  },
  data() {
    return {
      store,
    };
  },
};
</script>
<template lang="">
  <div
    class="bg-body container d-flex justify-content-center gap-5 p-5 flex-wrap"
  >
    <appCard
      v-for="(elem, index) in store.cardList"
      :key="index"
      :monster="elem"
    />
  </div>
</template>
<style lang="scss" scoped>
div.container {
  height: 80vh;
  overflow: auto;
}
</style>
