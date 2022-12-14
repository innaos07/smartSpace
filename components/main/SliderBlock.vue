<template>
  <div class="slider">
      <div 
        class="slider__list d-flex" 
        v-for="(item, index) in slider__list" :key="item.id"
      >
        <div 
          class="slider__item" 
          :class="slider__list[count-1] == slider__list[index] ? 'slider__item--current': ''"
        >
          <img :src="require(`@/assets/img/${item.img}.jpg`)" />
        </div>
      </div>

      <div class="slider__arrows arrows d-flex">
        <span 
          class="slider__arrow slider__arrow--prev"
          @click="showPrevSlider"  
        >
        </span>
        <span 
          class="slider__arrow slider__arrows--next"
          @click="showNextSlider"  
        >
        </span>
      </div>
  </div>
</template>

<script>
export default {
  props: {
    slider__list: {
      type: Array,
      default() {
        return {};
      },
    },
  },
  data () {
    return {
      count : 1,
    }
  },
  methods: {
    showPrevSlider() {
      this.count = this.count === 1 ? this.slider__list.length : this.count - 1; 
    },

    showNextSlider() {
      this.count = this.count === this.slider__list.length ? 1 : this.count + 1; 
    }
  }
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.slider {
  position: relative;
  flex: 1 0 100%;

  .slider__item {
    display: none;
    position: relative;
    width: 100%;
    height: 100%;
    
    &--current {
      display: flex;
    }
  }

  .slider__item img {
    width: 100%;
    height: 550px;
  }

  .slider__arrows {
    position: absolute;
    content: '';
    top: 20px;
    right: 20px; 
    column-gap: 30px;
  }

  .slider__arrow {
    width: 15px;
    height: 25px;
    background-image: url('@/assets/img/arrow.svg');
    background-repeat: no-repeat;
    background-position: 0 0;
    background-size: 100%;
    cursor: pointer;

    &--prev {
      transform: rotate(-180deg);
    }

    &:hover {
      filter: brightness(0) saturate(100%)
              invert(79%) sepia(5%) saturate(672%) 
              hue-rotate(175deg) brightness(82%) contrast(91%);    
    }

    &:active {
      opacity: 0.5;
    }
  }

  @media (max-width: $lg-width) {
    max-width: 550px;
  }

  @media (max-width: $md-width) {
    .slider__item img {
      height: 450px;
    }
  }

  @media (max-width: $sm-width) {
    max-width: 320px;

    .slider__item img {
      height: 350px;
    }
  }
}
</style>