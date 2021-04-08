<template>
  <section class="testimonial">
    <div class="testimonial__wrap">
      <div class="testimonial__text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat.
      </div>

      <div class="testimonial__number">99</div>

      <div class="testimonial__autor">
        <span class="testimonial__autor_name">DAVID JAMES</span
        ><span class="testimonial__autor_position">/ Web Design</span>
      </div>

      <div class="testimonial__rating">
        <div
          v-for="star in starArray"
          :key="star.id"
          class="testimonial__rating_stars"
        >
          <img :src="star.icon" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      starArray: [
        { id: 0, icon: 'star-black.svg' },
        { id: 1, icon: 'star-black.svg' },
        { id: 2, icon: 'star-black.svg' },
        { id: 3, icon: 'star-black.svg' },
        { id: 4, icon: 'star-grey.svg' },
      ],
    };
  },
};
</script>

<style lang ='scss' scoped>
.testimonial {
  display: flex;
  justify-content: center;
  align-items: center;

  height: 504px;

  // .testimonial__wrap
  &__wrap {
    display: flex;
    flex-direction: column;
  }

  // .testimonial__text

  &__text {
    margin: 0 0 31px 0;

    width: 735px;

    font-family: Open Sans;
    font-style: normal;
    font-weight: 300;
    font-size: 14px;

    line-height: 31px;
    letter-spacing: 0.896px;

    color: #373737;
  }

  // .testimonial__number
  &__number {
    margin: 0 0 29px 0;

    font-family: Open Sans;
    font-style: normal;
    font-weight: 300;
    font-size: 14px;

    line-height: 31px;
    letter-spacing: 0.896px;

    color: #373737;
  }

  // .testimonial__autor

  &__autor {
    margin: 0 0 25px 0;
    font-family: Oswald;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 27px;

    letter-spacing: 1.152px;

    &_name {
      color: #000000;

      text-transform: uppercase;
    }
    &_position {
      color: #252525;
      opacity: 0.3;
    }
  }

  // .testimonial__rating

  &__rating {
    display: flex;
    justify-content: center;

    position: relative;

    &_stars {
      width: 15px;
      height: 15px;

      margin: 0 0 29px 0;
    }

    &:after{
        display: block;

        position: absolute;
        bottom: 0;

        content: '';

        border-bottom: solid 2px #D8D8D8;

        width: 511px;
        opacity: 0.5;
    }

  }
}
</style>
