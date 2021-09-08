<template>
  <footer class="footer">
    <div class="footer__connection footer__width">
      <footer-card :cards="cards"></footer-card>
    </div>

    <div class="footer__width social-network">
      <div class="social-network__wrap">
        <div class="social-network__region font-style">
          3rd Floor, Santa Monica Beach, CA, San Francisco
        </div>

        <div class="social-network__adress font-style">
          (359) 0 123 456 789 - info@yourmail.com
        </div>

        <div class="social-network__wrap">
          <a
            href="#"
            class="social-network__link social-network__link_facebook"
          ></a>
          <a
            href="#"
            class="social-network__link social-network__link_twitter"
          ></a>
          <a
            href="#"
            class="social-network__link social-network__link_pinterest"
          ></a>
        </div>
      </div>
    </div>

    <div class="footer__copyright footer__width">
      Copyright 2016 - All Rights Reserved - Designed by JD
    </div>
  </footer>
</template>

<script>
import FooterCard from './FooterCard.vue';

export default {
  components: {
    FooterCard,
  },
  data() {
    return {
      cards: [
        {
          id: 0,
          icon: 'briefcase.svg',
          title: 'Want to work together?',
          text: 'Amazing. Tell us about your project!',
          textColor: '#373737',
          backgroundColor: '#FBFBFB',
        },
        {
          id: 1,
          icon: 'mail.svg',
          title: 'Contact us',
          text: 'Get in touch',
          textColor: '#FFFFFF',
          backgroundColor: '#70BD59',
        },
      ],
    };
  },
};
</script>

<style lang='scss' scoped>
.footer {
  display: flex;
  flex-direction: column;
  align-items: center;

  width: 95%;

  background: #252525;

  // .footer__connection
  &__connection {
    display: flex;
  }

  // .footer__copyright
  &__copyright {
    font-weight: 300;
    font-size: 13px;

    line-height: 19px;
    letter-spacing: 0.832px;

    color: #ffffff;

    mix-blend-mode: normal;
    opacity: 0.5;

    margin: 12px 0 21px;
  }

  &__width {
    width: 100%;
  }
}

.social-network {
  background: #2e2e2e;

  // .social-network__region
  &__region {
    margin: 136px 0 10px 0;
  }

  // .social-network__adress
  &__adress {
    margin: 0 0 39px 0;
  }

  // .social-network__link
  &__link {
    display: inline-block;

    width: 32px;
    height: 32px;

    margin: 0 10.5px 82px;

    background-repeat: no-repeat;
    cursor: default;

    // .social-network__link_facebook
    &_facebook {
      background: url("/facebook.svg");
    }

    // .social-network__link_twitter
    &_twitter {
      background: url("/twitter.svg");
    }

    // .social-network__link_pinterest
    &_pinterest {
      background: url("/pinterest-logo.svg");
    }
  }
}

// helper-classes
.font-style {
  font-weight: 300;
  font-size: 13px;

  line-height: 19px;
  letter-spacing: 0.832px;

  color: #ffffff;
  opacity: 0.5;
}
</style>
