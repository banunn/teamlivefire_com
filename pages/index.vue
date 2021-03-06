<template>
  <div>
    <home-hero />
    <get-started />
    <div class="wrap">
      <div class="row">
        <v-col id="focus" class="copy" sm="9" md="3">
          <h4 class="subline">Focus</h4>
          <p class="head-copy">
            We're bridging the gap between gun owners and professional training
          </p>
        </v-col>
      </div>
      <feature-block
        v-for="(b, idx) in blocks"
        :key="idx"
        :headline="b.headline"
        :body="b.body"
        :img="b.img"
        :reverse="b.reverse"
      />
    </div>
    <lf-mission></lf-mission>
    <div class="wrap">
      <lf-support></lf-support>
    </div>
  </div>
</template>

<script>
import homeHero from '@/components/home/hero'
import getStarted from '@/components/home/get_started'
import featureBlock from '@/components/home/feature-block'
import lfMission from '@/components/home/mission'
import lfSupport from '@/components/home/home-support'
export default {
  name: 'home_page',
  components: { homeHero, getStarted, featureBlock, lfMission, lfSupport },
  data: () => ({
    blocks: [
      {
        headline: 'Train with professionals',
        body: "Finding high quality, trustworthy and up-to-date training isn't easy. LiveFire takes all of the guesswork out by matching members with proven training, painstakingly developed by industry experts. Our trainers have spent decades training operators at the highest levels. Now, that expertise is available to firearms owners at any level.",
        img: require('~/assets/train-pros.png'),
        reverse: false,
      },
      {
        headline: 'TRACK YOUR PERFORMANCE',
        body: 'Built from the ground up, LiveFire enhances training at every level by leveraging personalized logging to ensure you are always improving. Train in any number of scenarios including live fire, dry fire, and instructional videos. When ready, you can even share your accomplishments with the LiveFire community at large!',
        img: require('~/assets/Track@3x.png'),
        reverse: true,
      },
      {
        headline: 'CONNECT WITH YOUR FRIENDS',
        body: 'The LiveFire community is the best place to share your training experiences with other members. Curious about how some of the world’s best trainers engage? LiveFire trainers and community leaders are always posting tips and training logs. Our community is always positive, encouraging, and constantly pushing each other to get better!',
        img: require('~/assets/Social2@3x.png'),
        reverse: false,
      },
    ],
  }),
  head: {
    script: [],
    meta: [
      {
        hid: 'description',
        name: 'description',
        content:
          'LiveFire is professional firearms training made accessible, approachable & affordable for everyone, everywhere. Now available for IOS  and Android devices!',
      },
    ],
  },
}
</script>

<style lang="scss" scoped>
.wrap {
  max-width: 1632px;
  padding: 0 64px;
  margin: 88px auto;
  @media (max-width: 1200px) {
    padding: 0 32px;
  }
  @media (max-width: 1000px) {
    padding: 0 24px;
  }
}

.copy {
  padding-left: 48px;
  border-left: 2px solid rgba(#000, 0.36);
  position: relative;
  padding-bottom: 0;
  .head-copy {
    display: block;
    position: relative;
    margin-bottom: 0;
    &::before {
      content: '';
      height: 100%;
      width: 3px;
      position: absolute;
      top: 0;
      bottom: 0;
      left: -49px;
      background: #000;
      display: block;
    }
  }
}

#focus {
  margin-bottom: 72px;

  @media (max-width: 1000px) {
    margin: 0 72px 72px 72px;
  }
}
</style>
