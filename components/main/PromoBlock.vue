<template>
  <section class="promo">
    <div class="promo__container container">
      <div class="promo__body row">
        <div class="col-6">
          <p class="promo__sub-title">RESIDENTIAL & OFFICE SPACES</p>
          <h1 class="promo__title">Smart Living Style for Smart People</h1>
          <p class="promo__description">
            Much did had call new drew that kept. Limits expect wonder law she.
            Now has you views woman noisy match money rooms.
          </p>
          <form action="#" class="promo__form form-search d-flex">
            <input
              type="text"
              placeholder="Enter Zipcode to search properties"
              class="form-search__input"
            />
            <a href="#" class="form-search__btn btn">Search Now!</a>
          </form>
        </div>

        <div class="col-6"></div>
      </div>
     <PromoItemBlock />
    </div>
  </section>
</template>

<script>
import PromoItemBlock from './PromoItemBlock.vue';
export default {
  components: { PromoItemBlock }
};
</script>

<style lang="scss">
@import "bootstrap/dist/css/bootstrap.css";
@import "@/assets/css/main.scss";

.promo {
  position: relative;
  padding-top: 184px;
  padding-bottom: 110px;
  z-index: 1000;

  &::after {
    content: '';
    position: absolute;
    top: 0;
    left: 68%;
    width: 100%;
    height: 100%;
    background-color: #bdccff;
  }

  .promo__sub-title {
    margin-bottom: 24px;
    font-weight: 700;
    font-size: 22px;
    line-height: 131.8%;
    text-transform: uppercase;
    color: #FF9900;
  }

  .promo__title {
    margin-bottom: 24px;
    font-weight: 800;
    font-size: 54px;
    line-height: 135%;
    color: #000000;
  }

  .promo__description {
    margin-bottom: 50px;
    font-size: 17px;
    line-height: 135%;
    letter-spacing: 0.01em;
  }

  .form-search {
    position: relative;
    margin-right: -188px;
    z-index: 20000;
    background-image: url("~assets/img/home.svg");
    background-color: #fff;
    background-repeat: no-repeat;
    background-position: 33px 32px;
    box-shadow: 0px 100px 80px rgba(0, 0, 0, 0.03), 0px 64.8148px 46.8519px rgba(0, 0, 0, 0.0227778), 0px 38.5185px 25.4815px rgba(0, 0, 0, 0.0182222), 0px 20px 13px rgba(0, 0, 0, 0.015), 0px 8.14815px 6.51852px rgba(0, 0, 0, 0.0117778), 0px 1.85185px 3.14815px rgba(0, 0, 0, 0.00722222);

    .form-search__input {
      width: 100%;
      padding: 30px 30px;
      padding-left: 75px;
      outline: none;
      background: transparent;
      border: 1px solid #DADADA;
      flex: 1 1 auto;

      &:focus {
        border-color: #F85A47;
      }
    }

    .form-search__btn {
      flex: 0 0 188px;
      height: 86px;
      padding: 30px 40px;
    }
  }
}
</style>