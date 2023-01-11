<template>
  <section class="header">
    <div class="header__body">
      <div class="container">
      <div class="header__content d-flex justify-content-md-between align-items-center">
        <a 
          href="#" 
          class="header__logo" 
          :class="{'header__logo--open' : isActive}"
        > 
          SmartSpace
        </a>
        <div  
          class="header__toggle menu-toggle d-md-none" 
          @click="isActive = !isActive"
        >
          <span class="menu-toggle__element"></span>
        </div>

        <nav class="header__menu menu d-none d-md-block">
          <ul class="menu__list d-flex flex-wrap">
            <li 
              class="menu__item" 
              v-for="item in menuList" 
              :key="item.name"
            >
              <a :href="item.link" class="menu__link">{{item.name}}</a>
            </li>
          </ul>
        </nav>

        <nav class="header__menu menu d-md-none">
          <ul 
            class="menu__list d-flex flex-column flex-wrap" 
            v-if="isActive" 
            :class="{'menu__list--open' : isActive}"
          >
            <li class="menu__item" :class="{'menu__item--open' : isActive}" v-for="item in menuList" :key="item.name">
              <a href="item.link" class="menu__link" :class="{'menu__link--open' : isActive}">{{item.name}}</a>
            </li>
          </ul>
        </nav>
      </div>    
    </div>
  </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      isActive: false,
      menuList: [
        {
          name: "Home",
          link: "#",
        },
        {
          name: "About",
          link: "#",
        },
        {
          name: "Service",
          link: "#",
        },
        {
          name: "Portfolio",
          link: "#",
        },
        {
          name: "Blog",
          link: "#",
        },
        {
          name: "Contact",
          link: "#",
        },
      ],
    }
  }

}
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.header {
  position: absolute; 
  top: 0;
  left: 0;
  width: 100%;

  .header__body {
    position: relative; 
    min-height: 101px;
    padding: 35px 0;
    z-index: 10000;
  }

  .header__logo {
    text-decoration: none;
    font-weight: 800;
    font-size: 23px;
    line-height: 134.8%;
    color: #31353B;
    transition: all 0.5s;

    &:hover,
    &:focus {
      color: #f85a47;
      outline: none;
    }

    &:active {
      opacity: 0.5;
    }
  }

  .menu-toggle {
    position: relative;
    width: 30px;
    height: 16px;
    cursor: pointer;  
    transition: 0.5s all;
    margin-left: auto;


      &::before,
      &::after, 
      span {
        content: "";
        position: absolute;
        left: 0;
        width: 100%;
        height: 2px;
        background-color: #31353B;
        transition: all 0.5s;
      }

      &::before {
        top: 8px;
      }

      &::after {
        top: 16px;
      }

      &:hover span,
      &:hover::before,
      &:hover::after, 
      &:focus span,
      &:focus::before,
      &:focus::after {
        background-color: #f85a47;
      }

      &:active span,
      &:active::before,
      &:active::after {
        opacity: 0.5;
      }
  }

  .menu {
    .menu__list {
      column-gap: 46px;
    }

    .menu__link {
      text-decoration: none;
      font-weight: 700;
      font-size: 13px;
      line-height: 130.8%;
      color: #000000;
      transition: 0.5s all;

      &:hover,
      &:focus {
        outline: none;
        color: #f85a47;
      }

      &:active {
        opacity: 0.5;
      }
    }
  }

  @media (max-width: $md-width) {
    position: fixed; 
    background-color: #fff;
    box-shadow: 0px 0px 21px -8px rgba(34, 60, 80, 0.2);
    z-index: 50000;

    .menu {
      .menu__list--open {
        position: absolute;
        top: 100px;
        left: 0;
        width: 100%;
        column-gap: 0;
        background-color: #fff;
        box-shadow: 0px 9px 5px -10px rgba(34, 60, 80, 0.2);

        &:first-child {
          border-top: 1px solid #DADADA;
        }
      }

      .menu__item--open {
        border-bottom: 1px solid #DADADA;
      }

      .menu__link--open {
        display: block;
        padding: 10px 50px;
        font-weight: 400;
        font-size: 16px;
        line-height: 130.8%;
        color: #000000;
      }
    }
  }
}

</style>