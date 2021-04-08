<template>
  <header class="header font-oswald">
    <picture>
      <img src="../assets/backheader.png" class="header__background" />
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
        <span>WHERE GREAT IDEAS COME TO LIFE</span>
      </div>

      <div class="header__subtitle">
        <span class="subtitle"
          >Passionate creative studio helping startups grow their
          business!</span
        >
      </div>

      <!-- TO DO slider component -->
      <div class="header__slide-control">
        <a href="#">01</a>
        <a href="#">02</a>
        <a href="#">03</a>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>

.header {
  position: relative;

  &__background {
    max-width: 1800px;
    max-height: 904px;
  }
  &__content {
    display: flex;
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
    margin: 0  0 303px 0;
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

// helper classes
.font-oswald {
  font-family: Oswald;
  font-style: normal;
}
</style>
