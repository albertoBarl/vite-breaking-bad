<template lang="">
  <div>
    <h4>Ci sono: {{ nResults }} elementi.</h4>
  </div>
</template>
<script>
import { store } from "../../assets/datas/store.js";
export default {
  data() {
    return {
      store,
    };
  },
  computed: {
    nResults() {
      return store.cardList.length;
    },
  },
};
</script>
<style lang="scss"></style>
