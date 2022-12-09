<template>
    <main>
        <PromoApp />
        <InstructionApp />
        <DealsApp />
    </main>
</template>

<script>
import InstructionApp from './main/InstructionApp.vue';
import PromoApp from './main/PromoApp.vue';
import DealsApp from './main/DealsApp.vue';

export default {
    components: { PromoApp, InstructionApp, DealsApp },
}
</script>

<style lang="scss">
@import "bootstrap/dist/css/bootstrap.css";
@import "@/assets/css/main.scss";
</style>