<template lang="">
  <select class="btn-body" v-model="value" @change="$emit('filter', value)">
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
export default {
  data() {
    return {
      archetypes: ["Dark Magician", "Alien", "Laval", "Cipher"],
      value: "Dark Magician",
    };
  },
};
</script>
<style lang="scss"></style>
