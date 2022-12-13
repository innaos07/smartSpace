<template>
  <section class="reviews">
    <div class="container">
      <h2 class="reviews__title header__title">
        Loved by businesses, and individuals across the globe.
      </h2>
      <div class="reviews__list row">
        <ReviewsItemBlock  
          v-for="item in reviewsList"   
          :key="item.id" 
          :item__reviews="item" 
        />
      </div>
      <ReviewsFooterBlock />
    </div>
  </section>
</template>

<script>
import ReviewsItemBlock from "./reviews/ReviewsItemBlock.vue";
import ReviewsFooterBlock from "./reviews/ReviewsFooterBlock.vue";

export default {
  components: { ReviewsItemBlock, ReviewsFooter },
  data () {
    return {
      reviewsList: [
        { 
          id: 23,
          author: 'Jane Cooper',
          location: 'Los Angeles, CA',
          avatar: 'avatar-01',
          text: 'Moderate children at of outweigh it. Unsatiable it considered invitation he travelling insensible. Consulted admitting oh mr up as described.',
          rating: 5,
          link: '#',
        },
        { 
          id: 24,
          author: 'Robert Fox',
          location: 'New York City, NY',
          text: 'The and collecting motionless difficulty son. His hearing staying ten colonel met. Sex drew six easy four dear cold',
          avatar: 'avatar-02',
          rating: 3,
          link: '#',
        },
        { 
          id: 25,
          author: 'Leslie Alexander',
          location: 'Buffalo, NJ',
          text: 'Sociable on as carriage my position weddings raillery consider. Peculiar trifling absolute and wandered vicinity property yet.',
          avatar: 'avatar-03',
          rating: 4,
          link: '#',
        }
      ],
    }
  }
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.reviews {
  padding-top: 100px;
  padding-bottom: 200px;

  .reviews__title {
    margin-bottom: 50px;
  }

  .reviews__list {
    margin-bottom: 50px;
  }

  @media (max-width: $lg-width) {
    padding: 60px 0;

    .reviews__list {
      row-gap: 30px;
    }
  }

  @media (max-width: $lg-width) {
    .reviews__title {
      margin-bottom: 30px;
    }
  }

  @media (max-width: $md-width) {
    padding-top: 10px;
  }

  @media (max-width: $sm-width) {
    padding-bottom: 30px;
  }
}

</style>