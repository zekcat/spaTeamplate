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

    <div class="">
      <card-teamplate :cards="cards"></card-teamplate>
    </div>
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
      cards: [
        {
          id: '0',
          image: 'camera.png',
          title: 'Photography',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
          description: '100 YEARS PHOTOGRAPHY',
        },
        {
          id: '1',
          image: 'cat.png',
          title: 'Photography',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
          description: 'A KITTEN’S LIFE',
        },
        {
          id: '2',
          image: 'computer.png',
          title: 'Photography',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
          description: 'GROOVEMADE PRODUCTS FOR MAC',
        },
        {
          id: '3',
          image: 'keyboard.png',
          title: 'Photography',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
          description: 'APPLE’s LOST MAGIC',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.latest-work {
  position: relative;

  height: 1859px;
  width: 1173px;

  // .latest-work__content
  &__content {
    position: absolute;

    top: 80px;
    left: 1px;
  }
}

.content {
  // .content__title
  &__title {
    margin: 0 0 50px 0;

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
}

.list {
  display: flex;

  &__link {
    margin: 0 41px 157px 0;

    font-family: Open Sans;
    font-weight: normal;
    font-size: 13px;

    text-transform: uppercase;
    text-decoration: none;

    line-height: 18px;
    letter-spacing: 0.832px;

    color: #252525;

    opacity: 0.3;

    &:hover {
      opacity: 1;
    }
  }
}

.image {
  position: absolute;
}
</style>
