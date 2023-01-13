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
  <div>
    <appCard
      v-for="(elem, index) in store.cardList"
      :key="index"
      :monster="elem"
    />
  </div>
</template>
<style lang="scss" scoped></style>
