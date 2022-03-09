<template>
  <section id="top" class="pt-16">
    <div
      class="flex flex-col items-center sm:flex-row sm:items-end pt-10 sm:pt-3 pb-5 sm:pb-10 bg-cover bg-bottom bg-center sm:bg-right bg-no-repeat sm:h-5/6 h-screen fv-bg"
      :style="{'background-image': 'url('+firstview+')'}"
    >
      <div class=" h-full w-11/12 sm:w-7/12 flex flex-col items-center sm:items-start justify-between pb-3 sm:pb-0 sm:pl-20">
        <h1>
          <img src="../../assets/img/index/firstview/firstview_v2_text.png" alt="定額の集客と定着に特化したワンストップツール" class="sm:w-10/12">
        </h1>
        <div class="sm:mt-10 w-10/12 sm:w-full flex flex-col ">
          <img src="../../assets/img/index/firstview/firstview_v2_sample.png" alt="" class="w-full">
        </div>
      </div>
      <div class="w-11/12 sm:w-5/12 text-center sm:pr-20">
        <a href="/contact.html" target="_blank">
          <ButtonL class="w-10/12 sm:w-10/12 border-4 border-white">今すぐ無料相談はこちら</ButtonL>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
import ButtonL from '../CommonParts/ButtonL.vue'
import FirstviewPC from "@/assets/img/index/firstview/firstviewbg_PC.png"
import FirstviewSP from "@/assets/img/index/firstview/firstviewbg_SP.png"

export default {
  name: 'Top',
  components: {
    ButtonL,
  },
  computed: {
    firstview(){
      if(window.innerWidth >= 640){
        return this.firstviewPC;
      }else{
        return  this.firstviewSP;
      }
    }
  },
  data(){
    return {
      firstviewPC: FirstviewPC,
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
