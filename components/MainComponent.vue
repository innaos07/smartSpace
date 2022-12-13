<template>
  <main>
    <PromoBlock />
    <InstructionBlock />
    <DealsBlock />
    <FeaturedBlock />
    <ReviewsBlock />
    <SubscribeBlock />
  </main>
</template>

<script>
import InstructionBlock from "./main/InstructionBlock.vue";
import PromoBlock from "./main/PromoBlock.vue";
import DealsBlock from "./main/DealsBlock.vue";
import FeaturedBlock from "./main/FeaturedBlock.vue";
import ReviewsBlock from "./main/ReviewsBlock.vue";
import SubscribeBlock from "./main/SubscribeBlock.vue";

export default {
  components: {
    PromoBlock,
    InstructionBlock,
    DealsBlock,
    FeaturedBlock,
    ReviewsBlock,
    SubscribeBlock,
  },
};
</script>

<style>

</style>
