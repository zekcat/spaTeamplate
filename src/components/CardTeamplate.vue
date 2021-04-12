<template>
  <section class="wrap-cards">
    <div v-for="item in cards" :key="item.id" class="wrap-cards__card card">
      <img :src="item.image" class="card__image" />

      <div class="card__text-wrap">
        <div class="card__title">
          {{ item.title }}
        </div>

        <div class="card__text">
          {{ item.text }}
        </div>

        <a href="#" class="card__button">read more</a>
      </div>

      <div class="card__desc">
        {{ item.description }}
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    cards: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang='scss' scoped>
.wrap-cards {
  display: flex;
  flex-direction: column;
  align-items: center;

  // .latest-work__card
  &__card {
    font-family: Open Sans;
    font-style: normal;
  }
}
.wrap-cards__card:nth-child(odd) {
  margin: 35px 0 0 0;

  text-align: right;

  align-self: flex-end;
  align-items: flex-end;

  .card__image {
    margin: 0 0 27px 0;
  }

  .card__text-wrap {
    margin: 0 26px 0 0;

    align-self: center;
  }

  .card__text {
    align-self: flex-end;
  }

  .card__desc {
    width: 80%;

    top: 261px;
    left: 4px;
  }
}

.wrap-cards__card:nth-child(even) {
  margin: -232px 0 -262px 0;

  text-align: left;

  align-self: flex-start;
  align-items: flex-start;

  .card__image {
    margin: 0 0 21px 0;
  }

  .card__text-wrap {
    margin: 0 48px 0 0;

    align-self: flex-end;
  }

  .card__desc {
    top: 264px;
    right: -32px;

    width: 43%;
  }
}

.card {
  display: flex;
  flex-direction: column;

  height: 596px;
  width: 585px;

  align-items: center;
  text-align: left;
  position: relative;

  // .card__image
  &__image {
    width: 453px;
    height: 443px;
  }

  // .card__title
  &__title {
    font-weight: 300;
    font-size: 18px;
    line-height: 25px;

    margin: 0 0 17px 0;

    letter-spacing: 1.152px;

    color: #252525;
  }

  // .card__text
  &__text {
    margin: 0 0 24px 0;

    width: 90%;

    font-weight: 300;
    font-size: 13px;

    line-height: 23px;
    letter-spacing: 0.832px;

    color: #c2c2c2;
  }

  // .card__button
  &__button {
    display: inline-block;

    visibility: hidden;

    font-weight: normal;
    font-size: 13px;

    text-decoration: line-through;
    text-decoration-color: #4caf50;
    text-transform: uppercase;

    line-height: 18px;
    letter-spacing: 0.832px;

    color: #252525;
  }

  &__text-wrap {
    display: flex;
    flex-direction: column;
  }
  // .card__desc
  &__desc {
    position: absolute;

    font-family: Oswald;
    font-weight: 300;
    font-size: 48px;

    line-height: 71px;
    letter-spacing: 3.072px;

    text-transform: uppercase;
    text-align: left;

    color: #252525;

    &_right {
      right: 0;
    }
    &_left {
      left: 0;
    }
  }

  &:hover &__button {
    visibility: visible;
  }
  &:hover &__desc {
    text-decoration: line-through;
    text-decoration-color: #4caf50;
  }
}
</style>
