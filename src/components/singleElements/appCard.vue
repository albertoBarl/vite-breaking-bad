<script>
export default {
  props: {
    monster: Object,
  },
};
</script>
<template lang="">
  <div class="card" style="width: 100px">
    <img :src="monster.card_images[0].image_url" alt="not available" />
    <span>{{ monster.name }}</span>
  </div>
</template>
<style lang="scss" scoped></style>
