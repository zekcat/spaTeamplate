<template>
  <section class="latest-work">
    <div class="latest-work__content content">
      <div class="content__title">Latest Works</div>
      <nav class="content__list list">
        <a href="" class="list__link">all</a>
        <a href="" class="list__link">web design</a>
        <a href="" class="list__link">branding</a>
        <a href="" class="list__link">photography</a>
        <a href="" class="list__link">illustration</a>
      </nav>
    </div>

    <card-teamplate
      :image="cameraImage"
      class="latest-work__image_first image"
    ></card-teamplate>
    <card-teamplate
      :image="catImage"
      class="latest-work__image_second image"
    ></card-teamplate>
    <card-teamplate
      :image="computerImage"
      class="latest-work__image_third image"
    ></card-teamplate>
    <card-teamplate
      :image="keyboardImage"
      class="latest-work__image_four image"
    ></card-teamplate>
  </section>
</template>

<script>
import CardTeamplate from './CardTeamplate.vue';

export default {
  components: {
    CardTeamplate,
  },
  data() {
    return {
      catImage: 'cat.png',
      cameraImage: 'camera.png',
      computerImage: 'computer.png',
      keyboardImage: 'keyboard.png',
    };
  },
};
</script>

<style lang="scss" scoped>
.latest-work {
  position: relative;
  height: 1989px;
  // .latest-work__content
  &__content {
    position: absolute;
    top: 204px;
    left: 315px;
  }

  // .latest-work__image
  &__image {

    &_first {
      top: 159px;
      right: 313px;
    }

    // .latest-work__image_second
    &_second {
      top: 519px;
      left: 308px;
    }

    // .latest-work__image_third
    &_third {
      top: 893px;
      right: 307px;
    }

    // .latest-work__image_four
    &_four {
      top: 1253px;
      left: 316px;
    }
  }
}
.content {
  // .content__title
  &__title {
    margin: 0 0 50px 0;

    font-family: Oswald;
    font-style: normal;
    font-weight: bold;
    font-size: 48px;
    line-height: 71px;
    letter-spacing: 3.072px;
    text-align: left;

    color: #252525;

    &:after {
      display: block;
      content: "";

      margin: 13px 0 0 0;
      width: 45px;
      border-bottom: 2px solid #252525;
    }
  }

  // .content__list
  &__list {
  }
}
.list {
  display: flex;

  &__link {
    margin: 0 40px 0 0;

    font-family: Open Sans;
    font-style: normal;
    font-weight: normal;
    font-size: 13px;
    line-height: 18px;

    text-transform: uppercase;
    text-decoration: none;

    letter-spacing: 0.832px;

    color: #252525;

    opacity: 0.3;

    &:hover{
        opacity: 1;
    }
  }
}
.image {
  position: absolute;
}
</style>
