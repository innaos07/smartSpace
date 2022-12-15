<template>
  <div class="social d-flex flex-sm-column justify-content-center align-items-center">
    <div 
      class="social__item"
      v-for="item in socialList" 
      :key="item.id"
    >
      <a  
        :href="item.link"
        class="social__link d-flex"
      >
        <img :src="require(`@/assets/img/${ item.icon }.svg`)" />
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      socialList: [
        { id: 1, icon: 'social-01', link: '' },
        { id: 2, icon: 'social-02', link: '' },
        { id: 3, icon: 'social-03', link: '' },
        { id: 4, icon: 'social-04', link: '' },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.social {
  position: fixed;
  top: 50%;
  right: 10px;
  gap: 25px;
  z-index: 4000;
  transform: translate(0px, -50%);

  .social__link {
    &:hover,
    &:focus {
      outline: none;
      filter: brightness(0) saturate(100%) invert(57%) sepia(43%) saturate(5848%) hue-rotate(332deg) brightness(98%) contrast(98%);
    }

    &:active {
      opacity: 0.5;
    }
  }

  .social__link img {
    width: 15px;
    height: 15px;
  }

  @media (max-width: $sm-width) {
    position: relative;
    top: 0;
    right: 0; 
    transform: translate(0px, 0px);
  }
}
</style>
