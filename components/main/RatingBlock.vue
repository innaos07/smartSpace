<template>
  <div class="rating d-flex">
    <div
      class="rating__item"
      v-for="star in starsList"
      :key="star"
      :class="item__rating >= star ? 'rating__item--active' : none"
    >
      <img src="@/assets/img/star.svg" alt="star" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item__rating: {
      type: Number,
      default: 1,
    },
  },
  data() {
    return {
      starsList: [1, 2, 3, 4, 5],
    };
  },
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.rating {
  .rating__item img {
    filter: brightness(0) saturate(100%) 
            invert(89%) sepia(30%) saturate(300%)
            hue-rotate(336deg) brightness(98%) contrast(92%);
  }

  .rating__item--active img {
    filter: none;
  }
}
</style>
