<template lang="">
  <select
    class="btn-body"
    v-model="store.selectedGen"
    @change="$emit('filter')"
  >
    <option
      v-for="(element, index) in archetypes"
      :value="element"
      :key="index"
    >
      Deck {{ element }}
    </option>
  </select>
</template>
<script>
import { store } from "../../assets/datas/store.js";
export default {
  data() {
    return {
      store,
      archetypes: ["Dark Margician", "Alien", "Laval", "Cipher"],
    };
  },
};
</script>
<style lang="scss"></style>
