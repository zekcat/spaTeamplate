<template>
  <a
    v-for="card in cards"
    :key="card.id"
    :style="{ 'background-color': card.backgroundColor, color: card.textColor }"
    class="card"
    href="#"
  >
    <img :src="card.icon" class="card__image" />

    <div class="card__title">{{ card.title }}</div>

    <div class="card__text">
      {{ card.text }}
    </div>
  </a>
</template>

<script>
export default {
  props: {
    cards: {
      type: Array,
      require: true,
    },
  },
};
</script>

<style lang='scss' scoped>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;

  cursor: default;

  width: 100%;

  text-decoration: none;
  // .card__image
  &__image {
    margin: 69px 0 19px 0;

    width: 35px;
    height: 35px;
  }

  // .card__title
  &__title {
    display: flex;
    align-items: flex-end;
    text-align: center;

    margin: 0 0 22px 0;

    font-weight: normal;
    font-size: 24px;

    line-height: 36px;
    letter-spacing: 2.66667px;
  }

  // .card__text
  &__text {
    margin: 0 0 100px 0;
  }

  &:link,
  &:visited {
    text-decoration: none;
  }
}
</style>
