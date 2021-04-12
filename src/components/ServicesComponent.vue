<template>
  <section class="service">
    <h1 class="service__title title">Our Services</h1>

    <div class="service__card-block card-block">
      <div class="card-block__card" v-for="item in cards" :key="item.id">
        <div class="card-block__card_title">{{ item.title }}</div>
        <div class="card-block__card_text">{{ item.text }}</div>

        <a href="#" class="card-block__card_link">read more</a>

        <img :src="item.icon" class="card-block__card_icon" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          id: '0',
          title: 'Branding',
          text:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.',
          icon: 'pencil-case.svg',
        },
        {
          id: '1',
          title: 'Design',
          text:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.',
          icon: 'graphic-design.svg',
        },
        {
          id: '2',
          title: 'Development',
          text:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.',
          icon: 'coding.svg',
        },
      ],
    };
  },
};
</script>

<style lang='scss' scoped>
.service {
  display: flex;
  flex-direction: column;
  align-items: center;

  height: 690px;

  padding: 124px 0 0 0;

  background: #fbfbfb;

  &__title {
    margin: 0 0 91px 16px;

    align-self: flex-start;
  }

  &__card-block {
    margin: 0 0 136px 0;
  }
}

.title {
  font-weight: bold;
  font-size: 48px;
  line-height: 71px;
  letter-spacing: 3.072px;

  color: #252525;

  &:after {
    display: block;
    content: "";

    margin: 7px 0 0 0;
    width: 45px;

    border-bottom: 2px solid #252525;
  }
}
.card-block {
  display: flex;
  justify-content: center;

  &__card {
    display: flex;
    flex-direction: column;

    position: relative;

    margin: 0 13px;
    width: 373px;
    height: 260px;

    font-weight: 300;

    background: #ffffff;

    &_title {
      display: block;
      margin: 45px 0 0 44px;

      font-size: 20px;
      line-height: 30px;
      letter-spacing: 1.28px;
      text-transform: uppercase;

      align-self: flex-start;

      color: #252525;

      &:after {
        display: block;
        content: "";

        margin: 15px 0 17px 0;
        width: 35px;

        border-bottom: 2px solid #252525;
      }
    }

    &_text {
      width: 284px;

      align-self: center;
      text-align: start;

      font-family: Open Sans;
      font-weight: normal;
      font-size: 12px;
      line-height: 25px;

      letter-spacing: 1.008px;

      color: #777777;
    }

    &_link {
      position: absolute;

      bottom: 41px;
      left: 45px;

      font-size: 10px;
      line-height: 15px;

      letter-spacing: 0.64px;
      text-transform: uppercase;
      text-decoration: none;

      color: #252525;

      opacity: 0.5;
    }

    &_icon {
      position: absolute;

      width: 50px;
      height: 50px;

      left: 275px;
      top: 50px;

      opacity: 0.4;

      background: #ffffff;
      box-shadow: 0px 0px 20px #dbdbdb;
    }

    &:hover &_icon,
    &:hover &_link {
      opacity: 1;
    }

    &:hover {
      border-bottom: 3px solid #70bf73;
    }
  }
}
</style>
