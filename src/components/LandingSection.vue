<template>
  <div class="row mt-2" style="background-color: white">
    <div class="col-lg-7">
      <img
        src="@/assets/Bitmap.png"
        srcset="@/assets/Bitmap@2x.png 2x, @/assets/Bitmap@3x.png 3x"
        class="img-fluid"
        alt="Responsive image"
      />
    </div>
    <div class="mt-3 offset-1 col-lg-3">
      <p class="headTitle">Subway Surfers</p>
      <p class="subTitle mb-1">SYBO Games</p>
      <p class="description">
        SURF the urban wave! <br />Dodge the incoming <br />
      </p>
      <p class="downloads">300k Downloads</p>
      <Button style="width: 75%; margin-right: 21%" text="More Info" />
    </div>
  </div>
</template>
<script>
import Button from "./Button.vue";

export default {
  components: { Button },
};
</script>

<style  scoped>
.row > * {
  padding: 0;
}
.headTitle {
  width: 100%;
  font-family: Tajawal;
  font-size: 24px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.05;
  letter-spacing: 0.2px;
  text-align: left;
  color: #3c3c3d;
  padding: 6px;
  margin: 1px;
}
.subTitle {
  width: 100%;
  font-family: Tajawal;
  font-size: 19.4px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.32;
  letter-spacing: normal;
  text-align: left;
  color: #444242;
  padding: 6px;
  margin: 1px;
}
.description {
  width: 100%;
  font-family: Tajawal;
  font-size: 21px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.36;
  letter-spacing: normal;
  text-align: left;
  color: #444242;
  padding: 6px;
  margin: 1px;
}
.downloads {
  width: 100%;
  opacity: 0.5;
  font-family: Tajawal;
  font-size: 12px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: 0.22px;
  text-align: left;
  color: #3c3c3d;
  padding: 6px;
  margin: 1px;
}
.img-fluid {
  width: 100%;
  max-width: 100%;
  height: 100%;
  padding: 0px;
  margin: 0px;
}
</style>