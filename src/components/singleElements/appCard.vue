<template lang="">
  <div class="card bg-warning border-0 text-center p-3" style="width: 200px">
    <img :src="monster.card_images[0].image_url" alt="not available" />
    <p>[ {{ monster.name }} ]</p>
    <span>- {{ monster.archetype }} -</span>
  </div>
</template>
<script>
export default {
  props: {
    monster: Object,
  },
};
</script>
<style lang="scss" scoped>
span {
  text-transform: uppercase;
}
</style>
