<template>
  <section id="top" class="pt-16">
    <div
      class="flex flex-col items-center sm:flex-row sm:items-end pt-6 pb-5 sm:pb-10 bg-cover bg-bottom bg-right bg-no-repeat sm:h-5/6 h-screen fv-bg"
      :style="{'background-image': 'url('+firstview+')'}"
    >
      <div class=" h-full w-11/12 sm:w-8/12 flex flex-col items-center sm:items-start justify-between pb-3 sm:pb-0 sm:pl-20">
        <h1>
          <img src="../../assets/img/index/firstview/firstview_v2_text.svg" alt="定額の集客と定着に特化したワンストップツール" class="h-full">
        </h1>
        <div class="sm:mt-10 sm:w-10/12 flex flex-col ">
          <img src="../../assets/img/index/firstview/firstview_v2_img.svg" alt="" class="w-full">
        </div>
      </div>
      <div class="w-11/12 sm:w-4/12 text-center sm:pr-20">
        <a href="/contact.html" target="_blank">
          <ButtonL class="w-full border-4 border-white">今すぐ無料相談はこちら</ButtonL>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
import ButtonL from '../CommonParts/ButtonL.vue'
import FirstviewBg from "@/assets/img/index/firstview/firstview_bg.png"
import FirstviewSP from "@/assets/img/index/firstview/firstview_SP.svg"

export default {
  name: 'Top',
  components: {
    ButtonL,
  },
  computed: {
    firstview(){
      if(window.innerWidth >= 640){
        return this.firstviewBg;
      }else{
        return  this.firstviewSP;
      }
    }
  },
  data(){
    return {
      firstviewBg: FirstviewBg,
      firstviewSP: FirstviewSP,
    }
  }
}
</script>

<style>
@media screen and (max-width: 640px) {
	/* 640px以下に適用されるCSS（スマホ用） */
  .fv-bg{
    height:calc(100vh - 64px);
  }
}
</style>
