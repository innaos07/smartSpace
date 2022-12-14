<template>
  <section class="promo">
    <div class="promo__container container">
      <div class="promo__body d-flex flex-column flex-lg-row">
        <PromoContentBlockVue />
        
        <div class="promo__slider d-flex justify-content-center">
          <SliderBlock :slider__list = "sliderList" />
        </div>
      </div>

     <PromoItemBlock />
    </div>
  </section>
</template>

<script>
import PromoContentBlockVue from './promo/PromoContentBlock.vue';
import PromoItemBlock from './promo/PromoItemBlock.vue';
import SliderBlock from './SliderBlock';

export default {
  components: { 
    PromoContentBlockVue, 
    PromoItemBlock, 
    SliderBlock 
  },
  data () {
    return {
      sliderList: [
        { id: 1, img: 'slider-01' },
        { id: 2, img: 'slider-02' },
        { id: 3, img: 'slider-03' }
      ],
    }
  }
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.promo {
  position: relative;
  padding-top: 184px;
  padding-bottom: 110px;
  overflow: hidden;

  &::after {
    content: '';
    position: absolute;
    top: 0;
    left: 68%;
    width: 100%;
    height: 100%;
    background-color: #bdccff;
  }

  .promo__body {
    position: relative;
    z-index: 1000;
  }

  .promo__slider {
    flex: 0 1 50%;
    position: relative;
    z-index: 20000;
  }

  @media (max-width: $lg-width) {
    padding-top: 160px;

    &::after {
      content: '';
      left: 55%;
    }

    .promo__slider {
      margin-bottom: 50px;
      flex: 0 1 100%;
    }
  }

  @media (max-width: $md-width) {
    padding-bottom: 70px;

    &::after {
      content: '';
      left: 68%;
    }

    .promo__slider {
      margin-bottom: 30px;
    }
  }
}
</style>