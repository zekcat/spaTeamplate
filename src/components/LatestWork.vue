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
      :image="catImage"
      class="latest-work__image_first image"
    ></card-teamplate>
    <card-teamplate
      :image="cameraImage"
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
  // .latest-work__content
  &__content {
    position: absolute;
  }

  // .latest-work__image
  &__image {
    position: absolute;
    // .latest-work__image_first

    &_first {
    }

    // .latest-work__image_second
    &_second {
    }

    // .latest-work__image_third
    &_third {
    }

    // .latest-work__image_four
    &_four {
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

      margin: 20px 0 0 0;
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
    margin: 0 20px;

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
}
</style>
