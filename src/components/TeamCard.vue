<template>
  <div v-for="item in teamCardArray" :key="item.id" class="card">
      <img :src="item.photo" class="card__photo" draggable="false"/>
    <div class="card__menu">
      <div class="card__menu-background"></div>
      <div class="card__name">{{ item.name }}</div>
      <div class="card__position">{{ item.position }}</div>
      <div class="card__description">{{ item.description }}</div>
    </div>
    <div class="card__men"></div>
  </div>
</template>

<script>
export default {
  props: {
    teamCardArray: {
      typeof: Array,
      require: true,
    },
  },
};
</script>

<style lang='scss' scoped>
.card {
  display: flex;
  flex-direction: column;

  position: relative;

  margin: 0 14px;
  color: #000000;
  &__photo {
    width: 370px;
    height: 398px;
  }

  // .card__name
  &__name {
    position: absolute;
    margin: 19px 0 0 0;

    width: 100%;

    font-family: Oswald;
    font-style: normal;
    font-weight: 300;
    font-size: 18px;

    line-height: 27px;
    letter-spacing: 1.152px;

    text-transform: uppercase;

    &::after {
      display: block;
      content: "";
      margin: 9px auto 6px;
      width: 45px;
      border-bottom: solid 2px #000000;
      //visibility: hidden;
      opacity: 0;
      transition: opacity 0.3s linear;
    }
  }

  // .card__position
  &__position {
    position: absolute;
    bottom: 0;

    width: 100%;

    opacity: 0;

    transition: bottom 0.5s, opacity 0.5s linear;

    font-family: Oswald;
    font-style: normal;
    font-weight: 300;
    font-size: 18px;

    line-height: 27px;
    letter-spacing: 1.152px;
  }

  &__description {
    position: absolute;
    bottom: 0;

    width: 100%;

    opacity: 0;

    transition: bottom 0.5s, opacity 0.5s linear;

    font-family: Open Sans;
    font-style: normal;
    font-weight: normal;
    font-size: 14px;

    color: #777777;
  }

  &__menu {
    position: absolute;
    bottom: 0;

    width: 100%;
    height: 55px;

    transition: height 0.5s;
  }

  &__menu-background {
    position: absolute;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: #ffffff;
    opacity: 0.5;
    transition: opacity 1s;
  }

  &__photo:hover ~ &__menu,
  &__menu:hover {
    height: 155px;
  }

  &__photo:hover ~ &__menu &__menu-background,
  &__photo:hover ~ &__menu &__name::after,
  &__menu:hover &__menu-background,
  &__menu:hover &__name::after {
    opacity: 1;
  }

  &__photo:hover ~ &__menu &__position,
  &__menu:hover &__position {
    bottom: 67px;
    opacity: 1;
  }

  &__photo:hover ~ &__menu &__description,
  &__menu:hover &__description {
    bottom: 30px;
    opacity: 1;
  }
}
</style>
