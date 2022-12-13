<template>
  <section class="footer">
    <div class="container">
      <div class="footer__body">
        <div class="container">
          <div class="footer__content d-flex flex-column flex-lg-row justify-content-md-between align-items-center">
            <a href="#" class="footer__logo"> SmartSpace </a>

            <nav class="footer__menu menu-footer">
              <ul class="menu-footer__list d-flex flex-wrap justify-content-center justify-content-lg-start">
                <li
                  class="menu-footer__item"
                  v-for="item in menuFooterList"
                  :key="item.name"
                >
                  <a href="item.link" class="menu-footer__link">{{ item.name }}</a>
                </li>
              </ul>
            </nav>
          </div>
          <div class="footer__copy">
            Copyright © 2021 AR Shakir . All Rights Reseved.
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      menuFooterList: [
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
    };
  },
};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";
.footer {

  .footer__body {
    padding-top: 60px;
    padding-bottom: 35px;
    border-top: 1px solid #DEDFE1;
  }

  .footer__content {
    margin-bottom: 75px;
  }

  .footer__logo {
    text-decoration: none;
    font-weight: 800;
    font-size: 23px;
    line-height: 134.8%;
    color: #31353b;
    transition: 0.5s all;

    &:hover {
      color: #5f5c70;
    }

    &:active {
      opacity: 0.5;
    }
  }

  .menu-footer {
    .menu-footer__list {
      column-gap: 46px;
      row-gap: 10px;
    }

    .menu-footer__link {
      text-decoration: none;
      font-weight: 700;
      font-size: 13px;
      line-height: 130.8%;
      color: #000000;
      transition: 0.5s all;

      &:hover {
        color: #5f5c70;
      }

      &:active {
        opacity: 0.5;
      }
    }
  }

  .footer__copy {
    font-weight: 700;
    font-size: 12px;
    line-height: 133.3%;
    text-align: center;
  }

  @media(max-width: $lg-width) {
    .footer__logo {
      margin-bottom: 30px;
    }

    .footer__content {
      margin-bottom: 50px;
    }
  }

  @media(max-width: $md-width) {
    .footer__content {
      margin-bottom: 30px;
    }

    .menu-footer__list {
      column-gap: 30px;
      row-gap: 10px;
    }

  }
}
</style>