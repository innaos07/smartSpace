<template>
  <div class="reviews__column col-12 col-lg-4 d-flex justify-content-center">
    <a :href="item__reviews.link" class="reviews__item item-reviews">
      <RatingBlock
        class="item-reviews__rating"
        :item__rating="item__reviews.rating"
      />
      <p class="item-reviews__text">{{ item__reviews.text }}</p>
      <div class="item-reviews__author author d-flex align-items-center">
        <div class="author__avatar d-flex align-items-center justify-content-center">
          <img
            :src="require(`@/assets/img/${item__reviews.avatar}.png`)"
            :alt="item__reviews.author"
          />
        </div>
        <div class="author__body d-flex flex-column">
          <span class="author__name">{{ item__reviews.author }}</span>
          <span class="author__location">{{ item__reviews.location }}</span>
        </div>
      </div>
    </a>
  </div>
</template>

<script>
import RatingBlock from "../RatingBlock.vue";

export default {
  components: { RatingBlock },
  props: {
    item__reviews: {
      type: Object,
      default() {
        return {};
      },
    },
  },
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.item-reviews {
  display: block;
  padding: 50px 40px;
  font: inherit;
  color: #333333;
  text-decoration: none;
  background: #ffffff;
  border: 1px solid #ebebeb;
  border-radius: 10px;
  transition: all 0.5s;

  &:hover {
    text-decoration: none;
    color: #333333;
    border: none;
    opacity: 0.6;
    box-shadow: 0px 100px 80px rgba(0, 0, 0, 0.03),
      0px 64.8148px 46.8519px rgba(0, 0, 0, 0.0227778),
      0px 38.5185px 25.4815px rgba(0, 0, 0, 0.0182222),
      0px 20px 13px rgba(0, 0, 0, 0.015),
      0px 8.14815px 6.51852px rgba(0, 0, 0, 0.0117778),
      0px 1.85185px 3.14815px rgba(0, 0, 0, 0.00722222),
      3px 44px 54px rgba(0, 0, 0, 0.08);
  }

  &:active {
    opacity: 1;
  }

  &:focus {
    outline: none;
    border: 1px solid #333333;
  }

  .item-reviews__rating {
    margin-bottom: 35px;
  }

  .item-reviews__text {
    margin-bottom: 50px;
    line-height: 175%;
  }

  .author {
    .author__avatar {
      margin-right: 20px;
    }

    .author__name {
      font-weight: 700;
      line-height: 137.5%;
    }

    .author__location {
      line-height: 118.8%;
    }
  }

  @media (max-width: $md-width) {
    padding: 40px 30px;

    .item-reviews__rating {
      margin-bottom: 30px;
    }

    .item-reviews__text {
      margin-bottom: 40px;
    }
  }

  @media (max-width: $sm-width) {
    padding: 30px 20px;

    .item-reviews__rating {
      margin-bottom: 20px;
    }

    .item-reviews__text {
      margin-bottom: 30px;
    }
  }
}
</style>
