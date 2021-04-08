<template>
  <footer class="footer">
    <div class="footer__connection">
      <footer-card :cardArray="cardArray"></footer-card>
    </div>
    <div class="footer__social-network social-network">
      <div class="social-network__wrap">
        <div class="social-network__region">
          3rd Floor, Santa Monica Beach, CA, San Francisco
        </div>
        <div class="social-network__adress">
          (359) 0 123 456 789 - info@yourmail.com
        </div>
        <div class="social-network__wrap">
          <a href="#" class="social-network__link_facebook"></a>
          <a href="#" class="social-network__link_twitter"></a>
          <a href="#" class="social-network__link_pinterest"></a>
        </div>
      </div>
    </div>
    <div class="footer__copyright">
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
      cardArray: [
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
  background: #252525;
  // .footer__connection
  &__connection {
    display: flex;
    width: 100%;
  }

  // .footer__social-network
  &__social-network {
  }

  // .footer__copyright
  &__copyright {
    width: 100%;

    font-family: Oswald;
    font-style: normal;
    font-weight: 300;
    font-size: 13px;

    line-height: 19px;
    letter-spacing: 0.832px;

    color: #ffffff;

    mix-blend-mode: normal;
    opacity: 0.5;
  }
}
.social-network {
  background: #2e2e2e;
  // .social-network__wrap
  &__wrap {
  }

  // .social-network__region
  &__region {
  }

  // .social-network__adress
  &__adress {
  }

  // .social-network__link
  &__link {
    // .social-network__link_facebook
    &_facebook {
        background: url("/mail.svg");
        background-repeat: no-repeat;
    }

    // .social-network__link_twitter
    &_twitter {
        background: url("/twitter.svg");
        background-repeat: no-repeat;
    }

    // .social-network__link_pinterest
    &_pinterest {
    }
  }
}
</style>
