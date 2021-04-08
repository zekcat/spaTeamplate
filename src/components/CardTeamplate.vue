<template>
  <div class="latest-work__card card">
    <img :src="image" class="card__image" />

    <div class="card__title">Photography</div>
    <div class="card__text">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit.
    </div>

    <a href="#" class="card__button">read more</a>

    <div class="card__desc"></div>
  </div>
</template>

<script>
export default {
  props: {
    image: {
      type: Image,
      required: true,
    },
  },
};
</script>

<style lang='scss' scoped>
.latest-work {
  // .latest-work__card
  &__card {
    font-family: Open Sans;
    font-style: normal;
  }
}
.card {
  // .card__image
  &__image {
    margin: 0 0 18px 0;
  }

  // .card__title
  &__title {
    margin: 0 0 0 11px;
    font-weight: 300;
    font-size: 18px;
    line-height: 25px;

    letter-spacing: 1.152px;

    color: #252525;
  }

  // .card__text
  &__text {
    font-weight: 300;
    font-size: 13px;
    line-height: 23px;
    align-items: center;
    letter-spacing: 0.832px;

    color: #c2c2c2;
  }

  // .card__button
  &__button {
    font-weight: normal;
    font-size: 13px;
    line-height: 18px;
    letter-spacing: 0.832px;

    color: #252525;
  }

  // .card__desc
  &__desc {
  }
}
</style>
