<template>
   <div class="promo__content">
      <p class="promo__sub-title">RESIDENTIAL & OFFICE SPACES</p>
      <h1 class="promo__title">Smart Living Style for Smart People</h1>
      <p class="promo__description">
        Much did had call new drew that kept. Limits expect wonder law she.
        Now has you views woman noisy match money rooms.
      </p>
      <form action="#" class="promo__form form-search d-flex flex-column flex-md-row">
        <input
          type="text"
          placeholder="Enter Zipcode to search properties"
          class="form-search__input"
        />
        <a href="#" class="form-search__btn btn">Search Now!</a>
      </form>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.promo__content {
    flex: 0 1 50%;
  
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
    z-index: 30000;
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
      padding: 30px;
      box-shadow: none;
    }
  }

  @media (max-width: $xl-width) {
    .promo__description {
       margin-bottom: 20px;
    }
  }

  @media (max-width: $lg-width) {
    margin-bottom: 50px;
    flex: 0 1 100%;

    .promo__description {
      margin-bottom: 30px;
    }

    .form-search {
      margin-right: 0;
    }
  }

  @media (max-width: $md-width) {
    margin-bottom: 40px;

    .promo__sub-title {
      margin-bottom: 15px;
      font-size: 18px;
    }

    .promo__title {
      font-size: 36px;
      font-weight: 700px;
    }

    .form-search {
      .form-search__btn {
        flex: 0 1 100%;
      }
    }
  }
}
</style>