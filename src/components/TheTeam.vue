<template>
  <section class="team">
    <div class="team__wrap-content">
      <div class="team__title">
        <span>The Team</span>
      </div>

      <div class="team__gallery-wrap">
        <team-card
          :teamCardArray="teamCardArray"
        ></team-card>
      </div>
    </div>
  </section>
</template>

<script>
import TeamCard from './TeamCard.vue';

export default {
  components: {
    TeamCard,
  },
  data() {
    return {
      teamCardArray: [
        {
          id: '0',
          name: 'Tom Jones',
          position: 'Director',
          description: 'Big boss',
          photo: 'tom-photo.png',
        },
        {
          id: '1',
          name: 'Michael Fraup',
          position: 'Creative Director',
          description: 'Create with simplicity in mind!',
          photo: 'mihael-photo.png',
        },
        {
          id: '2',
          name: 'Tim Cahill',
          position: 'Developer',
          description: 'create someone mb',
          photo: 'tim-photo.png',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.team {
  display: flex;
  justify-content: center;

  background: #fbfbfb;

  &__wrap-content{
    display: flex;
    flex-direction: column;

    align-items: flex-start;
  }

  // .team__title
  &__title {
    margin: 129px 0 0 14px;

    font-family: Oswald;
    font-style: normal;
    font-weight: bold;
    font-size: 48px;

    line-height: 71px;
    letter-spacing: 3.072px;

    color: #252525;

    &:after {
      display: block;
      content: "";

      margin: 20px 0 65px 0;
      width: 45px;

      border-bottom: 2px solid #252525;
    }
  }

  // .team__gallery-wrap
  &__gallery-wrap {
    display: flex;
    margin: 0 0 167px 0;
  }
}
</style>
