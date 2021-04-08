<template>
  <div
    v-for="card in cardArray"
    :key="card.id"
    :style="{ 'background-color': card.backgroundColor, color: card.textColor }"
    class="card"
  >
    <img :src="card.icon" class="card__image" />

    <div class="card__title">{{ card.title }}</div>
    <div class="card__text">
      {{ card.text }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    cardArray: {
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

  width: 100%;
  // .card__image
  &__image {
    margin: 69px 0 19px 0;
    width: 35px;
    height: 35px;
  }

  // .card__title
  &__title {
    margin: 0 0 22px 0;
  }

  // .card__text
  &__text {
    margin: 0 0 100px 0;
  }
}
</style>
