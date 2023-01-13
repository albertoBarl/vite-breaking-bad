<script>
export default {
  props: {
    monster: Object,
  },
};
</script>
<template lang="">
  <div class="card bg-dark text-white" style="width: 200px">
    <img :src="monster.card_images[0].image_url" alt="not available" />
    <p>{{ monster.name }}</p>
  </div>
</template>
<style lang="scss" scoped></style>
