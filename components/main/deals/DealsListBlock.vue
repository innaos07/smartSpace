<template>
  <div class="deals__list row">
    <div
      class="deals__column col-12 col-lg-4 d-flex justify-content-center"
      v-for="item in deals__list"
      :key="item.id"
    >
      <div class="deals__item item-deals d-flex justify-content-center">
        <div class="deals__options options d-flex">
          <a :href="item.linkOne" class="options__link">featured</a>
          <a :href="item.linkTwo" class="options__link">3D</a>
        </div>
        <a :href="item.linkImage" class="items-deals__link">
          <img :src="require(`@/assets/img/${item.img}.jpg`)" :alt="item.img" />
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    deals__list: {
      type: Array,
      default() {
        return {};
      },
    },
  },
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.deals__list {
  row-gap: 30px;

  .item-deals {
    position: relative;
  }
  .options {
    position: absolute;
    column-gap: 6px;
    top: 14px;
    left: 14px;
    z-index: 20000;

    .options__link {
      display: block;
      height: 26px;
      padding: 6px 12px;
      border: 1px solid #ffffff;
      border-radius: 5px;
      font-size: 12px;
      line-height: 1;
      text-align: center;
      color: #ffffff;
      background: rgba(0, 0, 0, 0.4);
      vertical-align: middle;
      text-decoration: none;
      transition: all 0.5s;

      &:hover,
      &:focus {
        outline: none;
        color: #f85a47;
      }

      &:active {
        color: #c4bbbb;
      }
    }
  }

  .items-deals__link {
    display: block;
    border-radius: 5px;
    overflow: hidden;
    transition: all 0.5s;

    &:focus {
      outline: none;
      border: 1px solid #c4bbbb; 
    }
  }

  .items-deals__link img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease 0.1s;

    &:hover {
      transform: scale(1.1);
    }
  }

  @media (max-width: $md-width) {
    .item-deals {
      max-width: 320px;
    }
  }
}
</style>