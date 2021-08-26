<template>
  <div>
    <div class="head">
      <img
        src="~/assets/logo_dark.webp"
        title="LiveFire Logo"
        alt="LiveFire Logo"
      />
    </div>
    <div class="row">
      <v-col sm="12" xs="12" md="8">
        <dl>
          <dt>General Info:</dt>
          <dd>info@teamlivefire.com</dd>
          <dt>Support:</dt>
          <dd>support@teamlivefire.com</dd>
          <dt>Location:</dt>
          <dd>
            <address>
              <span>8240 E 111th ST S, Unit C </span><br />
              <span>Bixby, OK 74008 </span>
            </address>
          </dd>
        </dl>
      </v-col>
      <v-col class="media" sm="12" xs="12" md="4">
        <p class="title">Media Inquiries:</p>
        <p class="body-copy">
          For press & media inquiries, please contact us by email at
          <span class="text-bold bold">connect@teamlivefire.com</span>
        </p>
        <a
          href="https://www.instagram.com/teamlivefire/"
          target="_blank"
          title="LiveFire on Instagram"
          ><img src="~/assets/icon_ig.webp" alt="" /></a
        ><a
          href="https://www.facebook.com/teamlivefire"
          target="_blank"
          title="LiveFire on Facebook"
          ><img src="~/assets/icon_fb.webp" alt=""
        /></a>
      </v-col>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home_support',
  data() {
    return {}
  },
}
</script>

<style lang="scss" scoped>
dl {
  display: grid;
  grid-template-columns: 1fr 1fr;
  @media (max-width: 1000px) {
    grid-template-columns: 1fr;
  }
  margin-top: 48px;
  gap: 24px 0;
  flex-wrap: wrap;
  width: 50%;
  display: grid;
  dt {
    flex: 1;
    font-weight: bold;
  }
  dd {
    flex: 1;
  }
}
.media {
  margin-top: 48px;
  a {
    display: inline-block;
    margin-right: 16px;
    &:last-child {
      margin-right: 0;
    }
  }
}
.bold {
  font-weight: bold;
}
</style>
