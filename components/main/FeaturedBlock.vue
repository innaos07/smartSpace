<template>
  <section class="featured">
    <div class="container">
      <h2 class="featured__title header__title text-center">
        Featured Listing of the Week
      </h2>
      <div class="featured__body row">
        <div class="featured__images col-12 col-lg-6 d-flex flex-column align-items-center">
          <div class="featured__image">
            <img src="@/assets/img/featured-01.jpg" alt="featured-01" />
          </div>
          <div class="featured__image featured__image--small">
            <img src="@/assets/img/featured-02.jpg" alt="featured-02" />
          </div>
        </div>
        <div class="featured__info info-featured col-12 col-lg-6 d-flex flex-column align-items-center align-items-lg-start">
          <h3 class="info-featured__title">
            The and collecting for <br class="d-lg-none" />
            the motionless difficulty son.
          </h3>
          <p class="info-featured__description">
            Conveying or northward offending admitting perfectly my. Colonel
            gravity get thought fat smiling add but difficult situations.
          </p>
          <div class="info-featured__options options-featured d-flex flex-wrap align-items-center justify-content-start">
            <div
              class="options-featured__item d-flex flex-column"
              v-for="item in optionsList"
              :key="item.title"
            >
              <span class="options-featured__title">{{ item.title }}</span>
              <span class="options-featured__text">{{ item.text }}</span>
            </div>
          </div>
          <a href="#" class="info-featured__btn btn">YES! I WANT BOOK “OFFICE PACKAGE”</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      optionsList: [
        { title: "Budget", text: "Confidential" },
        { title: "Size", text: "1200 m2" },
        { title: "Type", text: "Office" },
        { title: "Location", text: "Switzerland" },
        { title: "Status", text: "Done" },
        { title: "Flat", text: "8 Room" },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.featured {
  padding-top: 120px;
  padding-bottom: 100px;

  .featured__title {
    margin-bottom: 95px;
  }

  .featured__body {
    padding: 40px;
    padding-bottom: 80px;
    background: #f1ffff;
  }

  .featured__image--small {
    margin-top: -114px;
    margin-right: 20px;
    margin-left: 20px;
    filter: drop-shadow(0px 163px 80px rgba(0, 0, 0, 0.04))
      drop-shadow(0px 105.648px 46.8519px rgba(0, 0, 0, 0.0303704))
      drop-shadow(0px 62.7852px 25.4815px rgba(0, 0, 0, 0.0242963))
      drop-shadow(0px 32.6px 13px rgba(0, 0, 0, 0.02))
      drop-shadow(0px 13.2815px 6.51852px rgba(0, 0, 0, 0.0157037))
      drop-shadow(0px 3.01852px 3.14815px rgba(0, 0, 0, 0.00962963))
      drop-shadow(48px 58px 44px rgba(0, 0, 0, 0.09));
  }

  .info-featured {
    padding-top: 40px;
    padding-left: 50px;

    .info-featured__title {
      margin-bottom: 30px;
      font-weight: 600;
      font-size: 31px;
      line-height: 135.4%;
      color: #000000;
    }

    .info-featured__description {
      max-width: 320px;
      line-height: 150%;
      margin-bottom: 40px;
    }

    .info-featured__options {
      margin-bottom: 55px;
    }

    .info-featured__btn {
      max-width: 410px;
      min-height: 53px;
      padding: 16px 35px;
      border-radius: 5px;
      font-weight: 500;
      text-transform: uppercase;
      box-shadow: 0px 100px 80px rgba(248, 90, 71, 0.07),
        0px 64.8148px 46.8519px rgba(248, 90, 71, 0.0531481),
        0px 38.5185px 25.4815px rgba(248, 90, 71, 0.0425185),
        0px 20px 13px rgba(248, 90, 71, 0.035),
        0px 8.14815px 6.51852px rgba(248, 90, 71, 0.0274815),
        0px 1.85185px 3.14815px rgba(248, 90, 71, 0.0168519);
    }
  }

  .options-featured {
    max-width: 410px;
    column-gap: 80px;
    row-gap: 30px;

    .options-featured__item {
      flex: 1;
    }

    .options-featured__title {
      margin-bottom: 12px;
      font-weight: 700;
      font-size: 17px;
      line-height: 135.3%;
      color: #000000;
    }
  }

  @media (max-width: $xl-width) {
    .info-featured {
      padding-top: 0;
      padding-left: 15px;
    }
  }

  @media (max-width: $lg-width) {
    padding: 60px 0;

    .featured__title {
      margin-bottom: 50px;
    }

    .featured__images {
      margin-bottom: 70px;
    }

    .info-featured {
      padding: 0 50px;

      .info-featured__title {
        font-size: 26px;
        text-align: center;
      }

      .info-featured__description {
        max-width: 410px;
        margin-bottom: 30px;
      }

      .info-featured__options {
        margin-bottom: 40px;
      }
    }

    @media (max-width: $md-width) {
      .featured__title {
        margin-bottom: 30px;
      }
    }

    @media (max-width: $sm-width) {
      padding: 30px 0;

      .featured__body {
        padding-bottom: 40px;
      }

      .featured__images {
        margin-bottom: 50px;
      }

      .info-featured {
        padding: 0 15px;
      }
    }
  }
}
</style>