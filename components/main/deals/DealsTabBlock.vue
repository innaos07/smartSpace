<template>
  <ul class="deals__tabs tabs d-flex flex-column flex-lg-row align-items-center">
    <li
      class="tabs__item"
      v-for="item in deals__tabs"
      :key="item.name"
      @click="$emit('changeIsActive', item.id)"
    >
      <button
       type="button"
        class="tabs__btn"
        :class="isActive === item.id ? 'tabs__btn--current' : ''"
      >
        {{ item.name }}
      </button>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    deals__tabs: {
      type: Array,
      default() {
        return {};
      },
    },
    isActive: {
      type: Number,
      default: 12,
    },
  },
};
</script>


<style lang="scss">
@import "@/assets/css/variables.scss";

.deals__tabs {
  column-gap: 55px;
  margin-bottom: 45px;

  .tabs__item {
    .tabs__btn {
      border: none;
      background-color: transparent;
      text-decoration: none;
      font-weight: 400;
      font-size: 19px;
      line-height: 136.8%;
      color: #333333;
      transition: color 0.5s;

      &::before {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        width: 0;
        height: 1px;
        background-color: #f85a47;
        transition: width 0.5s ease 0s;
      }

      &:hover,
      &:focus {
        outline: none;
        color: #c4bbbb;
      }

      &:active {
        opacity: 0.5;
      }

      &--current {
        position: relative;
        font-weight: 600;
        color: #f85a47;

        &::before {
          width: 100%;
        }
        
        &:hover,
        &:active,
        &:focus {
          color: #f85a47;
        }
      }
    }
  }

  @media (max-width: $md-width) {
    column-gap: 0;
    row-gap: 10px;
  }
}
</style>