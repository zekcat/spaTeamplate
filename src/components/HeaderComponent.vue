<template>
  <header class="header font-oswald">
    <picture>
      <img :src="picked" class="header__background" />
    </picture>

    <div class="header__content">
      <nav class="header__menu menu">
        <a href="#" class="menu__link">works</a>
        <a href="#" class="menu__link">about</a>
        <a href="#" class="menu__link">services</a>
        <a href="#" class="menu__link">blog</a>
        <a href="#" class="menu__link">contact</a>
      </nav>

      <div class="header__headline headline">
        <span>{{ textHeadLine }}</span>
      </div>

      <div class="header__subtitle">
        <span class="subtitle"
          >{{textSubTitle}}</span
        >
      </div>

      <!-- TO DO slider component -->
      <div class="header__slide-control slide-control">
        <input
          name="slider"
          id="one"
          type="radio"
          :value="0"
          v-model="picked"
          class="slide-control_hide-input"
          :checked="buttonIsChecked === '0'"
        />
        <label for="one" class="slide-control__link">01</label>

        <input
          name="slider"
          id="two"
          type="radio"
          :value="1"
          v-model="picked"
          class="slide-control_hide-input"
          :checked="buttonIsChecked === '1'"
        />
        <label for="two" class="slide-control__link">02</label>

        <input
          name="slider"
          id="three"
          type="radio"
          :value="2"
          v-model="picked"
          class="slide-control_hide-input"
          :checked="buttonIsChecked === '2'"
        />
        <label for="three" class="slide-control__link">03</label>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      mainImage: '/backheader.png',
      textHeadLine: 'WHERE GREAT IDEAS COME TO LIFE',
      textSubTitle:
        'Passionate creative studio helping startups grow their business!',
      buttonIsChecked: '0',
      imageArray: {
        0: '/backheader.png',
        1: '/backheader1.jpg',
        2: '/backheader4.jpg',
      },
    };
  },
  computed: {
    picked: {
      get() {
        return this.mainImage;
      },
      set(value) {
        console.log(value);
        switch (value) {
          case 0:
            this.textHeadLine = 'WHERE GREAT IDEAS COME TO LIFE';
            this.textSubTitle = 'Passionate creative studio helping startups grow their business!';
            this.buttonIsChecked = '0';
            this.mainImage = this.imageArray['0'];
            console.log('0 maked');
            break;
          case 1:
            this.textHeadLine = 'WATCH IN FUTURE';
            this.textSubTitle = 'Studio helping startups grow their business!';
            this.buttonIsChecked = '1';
            this.mainImage = this.imageArray['1'];
            break;
          case 2:
            this.textHeadLine = 'LIFE WITH NEW IDEAS';
            this.textSubTitle = 'Passionate creative  grow their business!';
            this.buttonIsChecked = '2';
            this.mainImage = this.imageArray['2'];
            break;
          default:
        }
      },
    },
  },
  methods: {
    setBack(value) {
      switch (value) {
        case 0:
          this.mainImage = this.imageArray['0'];
          break;
        case 1:
          this.mainImage = this.imageArray['1'];
          break;
        case 2:
          this.mainImage = this.imageArray['2'];
          break;
        default:
      }
    },
  },
  mounted() {
    // this.picked = '0';
  },
};
</script>

<style lang="scss" scoped>
.header {
  position: relative;

  &__background {
    width: 1800px;
    height: 904px;
  }
  &__content {
    display: flex;
    position: relative;
    flex-direction: column;
    align-items: center;

    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;

    z-index: 10;
  }
  &__menu {
    width: 503px;
    height: 21px;

    margin: 79px 311px 283px 0;
    align-self: flex-end;
  }
  &__headline {
    margin: 0 25px 0 0;
  }
  &__subtitle {
    margin: 0 0 303px 0;
  }
  &__slide-control {
  }
}

.menu {
  display: flex;
  justify-content: space-around;

  &__link {
    position: relative;

    font-weight: normal;
    font-size: 14px;

    line-height: 21px;
    letter-spacing: 1.94px;

    color: #ffffff;
    text-transform: uppercase;
    text-decoration: none;

    &:after {
      position: absolute;
      content: "";
      display: block;
      right: 0;
      width: 20px;
      border-bottom: 2px solid #4caf50;
      transition: width 0.5s;
    }
    &:hover:after {
      width: calc(100%);
    }
  }
}
.headline {
  text-transform: uppercase;

  font-weight: 500;
  font-size: 72px;

  line-height: 107px;
  letter-spacing: 4.608px;

  color: #ffffff;
}
.subtitle {
  font-family: Open Sans;
  font-weight: normal;
  font-size: 20px;

  line-height: 27px;
  letter-spacing: 1.28px;

  color: #ffffff;
  opacity: 0.8;
}
.slide-control {
  display: flex;
  align-items: flex-end;

  &__link {
    margin: 0 4.5px;

    font-family: Oswald;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;

    line-height: 27px;
    letter-spacing: 1.152px;

    color: #ffffff;
    opacity: 0.4;
  }
  &_hide-input {
    display: none;

    &:checked + .slide-control__link {
      font-family: Oswald;
      font-style: normal;
      font-weight: bold;
      font-size: 36px;
      line-height: 53px;
      letter-spacing: 2.304px;

      color: #ffffff;
      opacity: 1;

      text-decoration: line-through;
      text-decoration-color: #4caf50;
    }
  }
}

// helper classes
.font-oswald {
  font-family: Oswald;
  font-style: normal;
}
</style>
