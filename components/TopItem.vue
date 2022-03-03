<template>
  <section id="top" class="pt-16">
    <div
      class="flex flex-col justify-between items-center py-10 bg-cover bg-right bg-no-repeat h-screen sm:h-full"
      :style="{'background-image': 'url('+firstview+')'}"
    >
      <div class="flex flex-col sm:flex-row items-center w-11/12 h-2/6">
        <div class="h-3/6 sm:mr-16">
          <img src="../assets/img/index/onestep/onestep_square.svg" alt="+one step" class="h-full">
        </div>
        <div>
          <h1 class="font-bold sm:text-5xl text-4xl text-center sm:text-left">
            <span style="background: linear-gradient(transparent 80%, #FFF34A 50%); line-height:74px;">
              集客・定着に
              <span class="text-2xl sm:text-3xl">特化した</span>
            </span>
            <br>
            <span style="background: linear-gradient(transparent 80%, #FFF34A 50%); line-height:74px;">
              ワンストップツール
            </span>
          </h1>
        </div>
      </div>
      <div class="flex flex-col sm:flex-row justify-between items-center sm:items-end w-11/12 h-2/6 sm:h-4/6 mt-16">
        <div class="h-4/6 sm:h-full flex items-end">
          <img class="h-full" src="../assets/img/index/firstview/system_sample.svg" alt="+one step">
        </div>
        <div class="w-9/10 sm:w-4/12">
          <ButtonL class="w-full border-2 border-white">
            <router-link to="/contact.html" target="_blank">今すぐ無料相談はこちら</router-link>
          </ButtonL>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ButtonL from './CommonParts/ButtonL.vue'
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

</style>
