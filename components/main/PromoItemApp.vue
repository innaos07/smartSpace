<template>
  <div class="partners">
    <p class="partners__title">Our Amazing Partners</p>
    <div class="partners__list d-flex align-items-center">
      <div 
        class="partners__item" 
        v-for="item in PartnerList" :key="item.img">
        <img :src="require(`@/assets/img/${item.img}.svg`)"/>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PromoItemApp',
  data() {
    return {
      PartnerList: [
        {name: "", img: "partner-01"},
        {name: "", img: "partner-02"},
        {name: "", img: "partner-03"},
        {name: "", img: "partner-04"},
        {name: "", img: "partner-05"},
        {name: "", img: "partner-06"},
      ],
    };
  },
};
</script>

<style lang="scss">
@import "bootstrap/dist/css/bootstrap.css";
@import "@/assets/css/main.scss";

.partners {
  position: relative;
  z-index: 20000;

  .partners__title {
    font-size: 17px;
    line-height: 135%;
    letter-spacing: 0.01em;
    color: #31353B;
  }

  .partners__list {
    column-gap: 50px;
  }
}
</style>