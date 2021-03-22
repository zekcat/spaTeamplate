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

<style>
</style>
