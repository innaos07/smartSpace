<template>
    <main>
        <PromoBlock />
        <InstructionBlock />
        <DealsBlock />
    </main>
</template>

<script>
import InstructionBlock from './main/InstructionBlock.vue';
import PromoBlock from './main/PromoBlock.vue';
import DealsBlock from './main/DealsBlock.vue';

export default {
    components: { PromoBlock, InstructionBlock, DealsBlock },
}
</script>

<style lang="scss">
@import "bootstrap/dist/css/bootstrap.css";
@import "@/assets/css/main.scss";
</style>