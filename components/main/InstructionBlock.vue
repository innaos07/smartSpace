<template>
  <section class="instruction">
    <div class="container">
      <h2 class="instruction__title header__title text-center">
        How it works?
      </h2>
      <div class="instruction__body row">
        <div
          class="instruction__column col-12 col-md-4 d-flex align-items-center justify-content-center"
          v-for="item in instructionList"
          :key="item.title"
        >
          <div class="instruction__item item-instruction d-flex flex-column align-items-center">
            <div 
              class="item-instruction__image d-flex justify-content-center align-items-center"
              :class="item.class"
            >
              <img :src="require(`@/assets/img/${item.icon}.svg`)" />
            </div>
            <h3 class="item-instruction__title">{{ item.title }}</h3>
            <p class="item-instruction__description">{{ item.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      instructionList: [
        {
          icon: "instruction-01",
          class: "item-instruction__image--purpure",
          title: "Research Suburbs",
          description:
            "Wonder twenty hunted and put income set desire expect. Am cottage calling.",
        },
        {
          icon: "instruction-02",
          class: "item-instruction__image--blue",
          title: "Instant Valuation",
          description:
            "Conveying or northward offending admitting perfectly my. Colonel gravit and moonlight.",
        },
        {
          icon: "instruction-03",
          class: "item-instruction__image--pink",
          title: "Track Property",
          description:
            "Moderate children at of outweigh it. Unsatiable it considered invitation he travelling insensible.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "bootstrap/dist/css/bootstrap.css";
@import "@/assets/css/main.scss";

.instruction {
  padding: 110px 0;

  .instruction__title {
    margin-bottom: 70px;
  }

  .instruction__column {
    &:first-child {
      opacity: 0.2;
    }
  }

  .item-instruction {
    padding: 0 30px;

    .item-instruction__image {
      width: 90px;
      height: 90px;
      margin-bottom: 50px;
      border-radius: 20px;
    }

    .item-instruction__image--purpure {
      background-color: #9672ff;
    }

    .item-instruction__image--blue {
      background-color: #4ddffd;
      box-shadow: 0px 100px 80px rgba(77, 223, 253, 0.07),
        0px 64.8148px 46.8519px rgba(77, 223, 253, 0.0531481),
        0px 38.5185px 25.4815px rgba(77, 223, 253, 0.0425185),
        0px 20px 13px rgba(77, 223, 253, 0.035),
        0px 8.14815px 6.51852px rgba(77, 223, 253, 0.0274815),
        0px 1.85185px 3.14815px rgba(77, 223, 253, 0.0168519);
    }

    .item-instruction__image--pink {
      background-color: #f2b8ec;
      box-shadow: 0px 100px 80px rgba(242, 184, 236, 0.07),
        0px 64.8148px 46.8519px rgba(242, 184, 236, 0.0531481),
        0px 38.5185px 25.4815px rgba(242, 184, 236, 0.0425185),
        0px 20px 13px rgba(242, 184, 236, 0.035),
        0px 8.14815px 6.51852px rgba(242, 184, 236, 0.0274815),
        0px 1.85185px 3.14815px rgba(242, 184, 236, 0.0168519);
    }

    .item-instruction__title {
      margin-bottom: 15px;
      font-weight: 600;
      font-size: 22px;
      line-height: 136.4%;
      color: #000000;
      text-align: center;
    }

    .item-instruction__description {
      line-height: 162%;
      text-align: center;
    }
  }

  @media(max-width: $lg-width) {
    padding: 60px 0;
  }

  @media (max-width: $md-width) {
    .instruction__body {
      row-gap: 30px;
    }

    .instruction__title {
      margin-bottom: 40px;
    }

    .instruction__column {
      &:first-child {
        opacity: 1;
      }
    }

    .item-instruction {
      max-width: 320px;
    }
  }

  @media (max-width: $md-width) {
    padding: 30px 0;

    .instruction__title {
      margin-bottom: 30px;
    }
  }
}
</style>