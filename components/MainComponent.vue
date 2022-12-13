<template>
    <main>
        <PromoBlock />
        <InstructionBlock />
        <DealsBlock />
        <FeaturedBlock />
        <ReviewsBlock />
    </main>
</template>

<script>
import InstructionBlock from './main/InstructionBlock.vue';
import PromoBlock from './main/PromoBlock.vue';
import DealsBlock from './main/DealsBlock.vue';
import FeaturedBlock from './main/FeaturedBlock.vue';
import ReviewsBlock from './main/ReviewsBlock.vue';

export default {
    components: { PromoBlock, InstructionBlock, DealsBlock, FeaturedBlock, ReviewsBlock },
}
</script>

<style lang="scss">
@import "bootstrap/dist/css/bootstrap.css";
@import "@/assets/css/main.scss";
</style>