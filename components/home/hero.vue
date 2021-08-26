<template>
  <div class="hero">
    <video autoplay loop src="~/assets/video_recolor_4.mp4">
      <img src="~/assets/hero_bg.webp" alt="" />
    </video>
    <div class="overlay"></div>
    <div class="lockup">
      <h1>Professional<br />Firearms Training</h1>
      <p>
        Made accessible, approachable & affordable for everyone, everywhere.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home_hero',
}
</script>

<style lang="scss" scoped>
.hero {
  position: relative;
  width: 100%;
  video {
    width: 100%;
    @media (max-width: 1000px) {
      height: 90vh;
      width: 100%;
      object-fit: cover;
    }
  }
  .overlay {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: linear-gradient(transparent, transparent, #000000);
  }
  .lockup {
    z-index: 1;
    position: absolute;
    left: 50%;
    top: 64px;
    transform: translate(-50%, 0%);
    text-align: center;
    color: #000;
    @media (max-width: 1480px) {
      top: 32px;
      left: inherit;
      width: 100%;
      transform: inherit;
      padding: 24px;
    }
    h1 {
      line-height: 1.5em;
      text-align: center;
      font-size: 64px;
      text-transform: uppercase;
      margin: 0;
      font-weight: 300;
      @media (max-width: 1480px) {
        top: 64px;
        font-size: 32px;
      }
    }
    p {
      margin: 0;
      line-height: 1.8em;
      text-align: center;
      font-size: 24px;
      @media (max-width: 1480px) {
        font-size: 17px;
        padding-top: 12px;
      }
    }
  }
}
</style>
