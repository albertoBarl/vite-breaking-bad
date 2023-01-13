<script>
import appCard from "./singleElements/appCard.vue";
import { store } from "../assets/datas/store.js";

export default {
  appCard,
  data() {
    return {
      store,
    };
  },
};
</script>
<template lang="">
  <div>
    <appCard v-for="(elem, index) in store.data" :key="index" :monster="elem" />
  </div>
</template>
<style lang="scss" scoped></style>
