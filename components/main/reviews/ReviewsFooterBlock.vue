<template>
  <div class="reviews__footer footer-reviews d-flex flex-column flex-lg-row align-items-center">
    <div class="footer-reviews__partners partners-footer-reviews row order-2 order-lg-1">
      <div
        class="partners-footer-reviews__item d-flex col-12 col-sm-6 col-md-4 col-lg-2 align-items-center justify-content-center"
        v-for="item in partnerFooterList"
        :key="item.img"
      >
        <img :src="require(`@/assets/img/${item.img}.svg`)" :alt="item.name" />
      </div>
    </div>
    <div class="footer-reviews__info order-1 order-lg-2">
      <p class="footer-reviews__text">
        Give us a Call 1-888-111-2222 and we can set you up, or
        <a href="#" class="footer-reviews__link">check our pricing plans</a>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      partnerFooterList: [
        { name: "partner01", img: "partner-footer-01" },
        { name: "partner02", img: "partner-footer-02" },
        { name: "partner03", img: "partner-footer-03" },
        { name: "partner04", img: "partner-footer-04" },
        { name: "partner05", img: "partner-footer-05" },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";
.footer-reviews {
  .partners-footer-reviews {
    flex: 1;
  }

  .footer-reviews__info {
    width: 310px;
    margin-left: auto;

    .footer-reviews__text {
      margin: 0;
      line-height: 1.5;
    }

    .footer-reviews__link {
      font: inherit;
      text-decoration: underline;
    }
  }

  @media (max-width: $lg-width) {
    .partners-footer-reviews {
      row-gap: 30px;
    }

    .partners-footer-reviews__item {
      height: 25px;
    }

    .footer-reviews__info {
      width: 100%;
      margin-bottom: 40px;
      margin-left: 0;
      text-align: center;
    }
  }

  @media (max-width: $md-width) {
    .footer-reviews__info {
      margin-bottom: 30px;
    }
  }
}
</style>
