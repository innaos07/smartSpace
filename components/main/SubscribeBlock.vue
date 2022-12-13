<template>
  <section class="subscribe">
    <div class="container">
      <div class="subscribe__body d-flex flex-column align-items-center">
        <h2 class="subscribe__title">Get Our Newsletter</h2>
        <p class="subscribe__description">To join the worldwide community</p>
        <form action="#" class="subscribe__form form-subscribe d-flex flex-column flex-md-row align-items-md-center">
          <div class="form-subscribe__content d-flex flex-column">
            <label for="subscribe" class="form-subscribe__label">Type your Email Address</label>
            <input type="email" class="form-subscribe__input" id="subscribe" name="subscribe" required placeholder="shakir260@gmail.com"/>
          </div>
          <button class="form-subscribe__btn btn" type="submit">Send Now</button>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
export default {

};
</script>

<style lang="scss">
@import "@/assets/css/variables.scss";

.subscribe {
  padding: 160px 0;
  background: #FBFCFC;

  .subscribe__title {
    margin-bottom: 10px;
    font-weight: 700;
    font-size: 45px;
    line-height: 144.2%;
    letter-spacing: 0.02em;
  }

  .subscribe__description {
    margin-bottom: 35px;
    font-weight: 700;
    font-size: 23px;
    line-height: 144.2%;
    letter-spacing: 0.02em;
  }

  .form-subscribe {
    max-width: 680px;
    width: 100%;
    padding: 25px 45px; 
    column-gap: 15px;
    background-color: #fff;
    box-shadow: 0px 163px 80px rgba(0, 0, 0, 0.04),
                0px 105.648px 46.8519px rgba(0, 0, 0, 0.0303704), 
                0px 62.7852px 25.4815px rgba(0, 0, 0, 0.0242963), 
                0px 32.6px 13px rgba(0, 0, 0, 0.02), 
                0px 13.2815px 6.51852px rgba(0, 0, 0, 0.0157037), 
                0px 3.01852px 3.14815px rgba(0, 0, 0, 0.00962963);

    .form-subscribe__content {
      flex: 1;
    }

    .form-subscribe__label {
      margin-bottom: 0;
      font-weight: 500;
      font-size: 17px;
      line-height: 144.2%;
      letter-spacing: 0.02em;
      opacity: 0.2;
    }

    .form-subscribe__input {
      width: 100%;
      min-height: 40px;
      border: none;
      outline: none;
      font-weight: 700;
      font-size: 20px;
      line-height: 144.2%;
      letter-spacing: 0.02em;
    }

    .form-subscribe__btn {
      min-height: 72px;
      padding: 23px 40px;
    }
  }

  @media(max-width: $lg-width) {
    padding: 60px 0;
  }

  @media(max-width: $md-width) {
    .subscribe__title {
      font-size: 30px;
    }

    .subscribe__description {
      margin-bottom: 30px;
      font-size: 18px;
    }

    .form-subscribe__content {
      margin-bottom: 20px;
    }

    .form-subscribe__btn {
      width: 100%;
    }
  }

  @media (max-width: $md-width) {
    padding-top: 30px;
    padding-bottom: 60px;
  }
}
</style>
