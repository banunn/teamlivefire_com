<template>
  <v-parallax dark height="700" :src="require('~/assets/mission.webp')">
    <div class="wrap">
      <div class="copy-block">
        <div class="copy">
          <h3 class="subline">Our Mission</h3>
          <p class="head-copy">
            No matter your mission, ours is simply to empower you to be ready.
          </p>
          <p class="body-copy">
            What is your motivation? Whether you have just purchased your first
            firearm, and want to understand how to safely use it, want to better
            understand how to protect yourself or your household, or looking to
            gain a competitive edge in national competitions, LiveFire is built
            for you. Our mission is to prepare you for yours. Regardless of
            experience level, LiveFire is excited to welcome you.
          </p>
        </div>
      </div>
    </div>
  </v-parallax>
</template>

<script>
export default {
  name: 'misson_component',
}
</script>

<style lang="scss" scoped>
.wrap {
  max-width: 1632px;
  padding: 0 16px;
  margin: 88px auto;
  @media (max-width: 1000px) {
    padding: 0;
  }
}
.copy-block {
  background: #000;
  border-radius: 24px;
  padding: 36px 48px;
  max-width: 35%;
  transition: all 0.35s ease;
  @media (max-width: 1450px) {
    max-width: 45%;
  }
  @media (max-width: 1350px) {
    max-width: 65%;
  }
  @media (max-width: 1350px) {
    max-width: 85%;
  }
  @media (max-width: 1000px) {
    padding: 16px 16px;
    max-width: 100%;
    max-height: 650px;
    margin: 24px 0;
  }
}
.copy {
  border-left: 1px solid rgba(#fff, 0.36);
  position: relative;
  padding: 36px 48px;
  @media (max-width: 1000px) {
    padding: 16px 16px;
    transform: scale(0.85);
  }
  .head-copy {
    display: block;
    position: relative;
    &::before {
      content: '';
      height: 100%;
      width: 2px;
      position: absolute;
      top: 0;
      bottom: 0;
      left: -48px;
      background: #fff;
      display: block;
      @media (max-width: 1000px) {
        left: -16px;
      }
    }
  }
}

.subline {
  font-size: 14px;
  text-transform: uppercase;
  font-weight: 400;
  margin-bottom: 36px;
}
.head-copy {
  letter-spacing: 0.08em;
  line-height: 1.8em;
  font-size: 24px;
}
.body-copy {
  font-size: 16px;
  line-height: 1.8em;
}
</style>
