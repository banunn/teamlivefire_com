<template>
  <div class="block">
    <div class="wrap row">
      <v-col md="5" sm="12">
        <div class="copy">
          <h4 class="subline">Get Started</h4>
          <p class="head-copy">
            Guided training from the world's most elite firearms instructors.
            Plus a whole lot more.
          </p>
          <div class="cta d-none d-md-block">
            <p class="body-copy mb-8">
              Scan this code to download<br />the LiveFire Training App.
            </p>
            <img
              height="143px"
              width="143px"
              title="Scan the and Download with the LiveFire QR Code"
              src="~/assets/lf_qr.webp"
              alt=""
            />
          </div>
          <div class="cta d-md-none">
            <a class="dl-link" href="#">
              <img
                width="165px"
                height="51px"
                src="~/assets/dl_ios.png"
                alt="Download LiveFire on IOS"
            /></a>
            <a class="dl-link" href="#">
              <img
                src="~/assets/dl_gp.png"
                width="165px"
                height="51px"
                alt="Download LiveFire on Google Play"
            /></a>
          </div>
        </div>
      </v-col>
    </div>
  </div>
</template>

<script>
export default {
  name: 'get_started',
  data: () => ({
    title: 'Get Started',
    links: [
      {
        link: 'https://apps.apple.com/us/app/livefire/id1563809934',
        title: 'Download LiveFire on Google Play!',
        alt: '',
        img: '~/assets/dl_ios.png',
      },
      {
        link: 'https://play.google.com/store/apps/details?id=com.teamlivefire.livefire&hl=en_US&gl=US',
        title: 'Download LiveFire on Google Play!',
        alt: '',
        img: '~/assets/dl_gp.png',
      },
    ],
  }),
}
</script>

<style lang="scss" scoped>
.block {
  background: #000;
  color: #fff;
  padding: 225px 24px 225px 24px;
  transition: all 0.34s ease;
  background: #000 url('~assets/download.webp') no-repeat bottom right;
  @media (max-width: 1400px) {
    padding: 125px 36px;
    background-size: 70%;
  }
  @media (max-width: 1000px) {
    padding: 72px 24px;
    min-height: 100vh;
    background-size: 100%;
    background-position: bottom center;
  }
  .wrap {
    max-width: 1400px;
    margin: 0 auto;
  }
}

.copy {
  padding-left: 48px;
  border-left: 1px solid rgba(#fff, 0.36);
  position: relative;

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
    }
  }
}

.dl-link {
  display: block;
  margin-bottom: 8px;
  max-width: 165px;
  img {
    max-width: 100%;
  }
}
</style>
