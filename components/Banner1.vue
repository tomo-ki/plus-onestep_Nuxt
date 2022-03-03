<template>
  <section id="Banner1">
    <div
      class="flex flex-col items-center justify-between py-10 bg-cover bg-right bg-no-repeat"
      :style="{'background-image': 'url('+banner1Bg+')'}"
    >
      <div class="bannerComment-w w-9/10 mb-6">
        <h2 class="bannerComment w-8/12 py-10">
          <span class=" text-xl font-bold leading-8" style="background: linear-gradient(transparent 80%, #FFF34A 50%);">
            お申し込みは簡単！
          </span>
          <br>
          <span class=" text-xl font-bold leading-8" style="background: linear-gradient(transparent 80%, #FFF34A 50%);">
            まずはご相談ください
          </span>
        </h2>
      </div>
      <div class="w-9/10">
        <ButtonXL class="w-full"><router-link to="/contact.html" target="_blank">今すぐ無料相談はこちら</router-link></ButtonXL>
      </div>
    </div>
  </section>
</template>

<script>
import ButtonXL from './CommonParts/ButtonXL.vue'
import Banner1Bg from "@/assets/img/index/banner/banner1.svg"

export default {
  name: 'Banner1',
  components: {
    ButtonXL,
  },
  data(){
    return {
      banner1Bg: Banner1Bg,
    }
  }
}
</script>

<style scoped>
.bannerComment-w{
  position: relative;
  display: inline-block;
}
.bannerComment::before, .bannerComment::after{
  position: absolute;
  margin: auto;
  content: "";
  left:0;
  vertical-align: middle;
  width: 60%;
  height: 1px;
  padding: 0;
  background-color: #6B6B6B;
}
.bannerComment::before{
  top: 20px;
  -webkit-transform: rotate(7deg);
  transform: rotate(7deg);
}
.bannerComment::after{
  top: 130px;
  -webkit-transform: rotate(-7deg);
  transform: rotate(-7deg);
}
</style>
