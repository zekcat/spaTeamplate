<template>
  <section class="about">
    <div class="about__wrap">
      <h1 class="about__title title">WE ARE</h1>
      <h1 class="about__caption caption">THE SQWD</h1>

      <div class="about__subtitle about__subtitle_first subtitle">
        <div class="subtitle__line"></div>
        <p class="subtitle__text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt.
        </p>
      </div>

      <div class="about__subtitle about__subtitle_second subtitle">
        <div class="subtitle__line"></div>
        <p class="subtitle__text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt.
        </p>
      </div>

      <img
        src="../assets/aboutphoto.png"
        class="about__image about__image_first"
      />
      <div class="about__rectangle"></div>
      <img
        src="../assets/aboutphoto2.png"
        class="about__image about__image_second"
      />
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang='scss' scoped>
.about {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 825px;

  &__wrap {
    position: relative;

    width: 1191px;
    height: 583px;
  }
  &__title {
    position: absolute;
    top: 67px;
    left: 10px;
  }

  &__caption {
    position: absolute;

    top: 118px;
    left: 10px;
    z-index: 15;
  }

  &__subtitle {
    position: absolute;

    &_first {
      top: 242px;
      left: 31px;

      z-index: 15;
    }
    &_second {
      bottom: 81px;
      right: 0px;

      z-index: 10;
    }
  }

  &__image {
    width: 309px;
    height: 418px;

    position: absolute;

    &_first {
      width: 309px;
      height: 391px;

      top: 24px;
      left: 203px;

      z-index: 10;
    }
    &_second {
      width: 309px;
      height: 391px;

      bottom: 0px;
      right: 258px;
    }
  }

  &__rectangle {
    position: absolute;
    top: 86px;
    left: 413px;

    width: 309px;
    height: 418px;

    background: #4caf50;
    opacity: 0.8;

    z-index: 5;
  }
}
.title {
  font-family: Oswald;
  font-style: normal;
  font-weight: bold;
  font-size: 36px;
  line-height: 53px;
  display: flex;
  align-items: flex-end;
  letter-spacing: 2.304px;

  color: #333333;
}
.caption {
  font-family: Open Sans;
  font-style: normal;
  font-weight: 300;
  font-size: 42px;
  line-height: 57px;
  display: flex;
  align-items: flex-end;
  letter-spacing: 2.688px;

  color: #504e4e;
}
.subtitle {
  display: flex;

  &__line {
    margin: 13px 10px 0 0;
    width: 20px;
    height: 3px;

    background: #353535;
  }
  &__text {
    width: 280px;

    margin: 0;

    font-family: Open Sans;
    font-style: normal;
    font-weight: 300;
    font-size: 15px;
    line-height: 25px;
    text-align: left;
    letter-spacing: 1.26px;

    color: #5b5858;
  }
}
</style>
