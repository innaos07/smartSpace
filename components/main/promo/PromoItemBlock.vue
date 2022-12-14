<template>
  <div class="partners">
    <p class="partners__title">Our Amazing Partners</p>
    <div class="partners__list row">
      <div 
        class="partners__item col-6 col-sm-4 col-md-2 d-flex align-items-center justify-content-center justify-content-md-start" 
        v-for="item in partnerList" :key="item.img">
        <img :src="require(`@/assets/img/${item.img}.svg`)" :alt="item.name"/>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PromoItemBlock',
  data() {
    return {
      partnerList: [
        { name: "partner-01", img: "partner-01" },
        { name: "partner-02", img: "partner-02" },
        { name: "partner-03", img: "partner-03" },
        { name: "partner-04", img: "partner-04" },
        { name: "partner-05", img: "partner-05" },
        { name: "partner-06", img: "partner-06" },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.partners {
  position: relative;
  z-index: 20000;

  .partners__title {
    margin-bottom: 30px;
    font-size: 17px;
    line-height: 135%;
    letter-spacing: 0.01em;
    color: #31353B;
  }

  .partners__list {
    row-gap: 20px;
  }

  @media (max-width: $md-width) {
    .partners__title {
      text-align: center;
    }
  }
}
</style>