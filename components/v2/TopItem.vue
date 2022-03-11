<template>
  <section id="top" class="pt-16">
    <div
      class="flex flex-col items-center sm:flex-row sm:items-end pt-10 sm:pt-3 pb-5 sm:pb-10 bg-cover bg-bottom bg-center sm:bg-right bg-no-repeat sm:h-5/6 h-screen fv-bg"
      :style="{'background-image': 'url('+firstview+')'}"
    >
      <div class=" h-full w-11/12 sm:w-7/12 flex flex-col items-center sm:items-start justify-between pb-3 sm:pb-0 sm:pl-20">
        <h1 class="anim1">
          <img src="../../assets/img/index/firstview/firstview_v2_text.png" alt="定額の集客と定着に特化したワンストップツール" class="sm:w-10/12">
        </h1>
        <div class="sm:mt-10 w-10/12 sm:w-full flex flex-col anim2">
          <img src="../../assets/img/index/firstview/firstview_v2_sample.png" alt="" class="w-full">
        </div>
      </div>
      <div class="w-11/12 sm:w-5/12 text-center sm:pr-20 anim3">
        <a href="/contact.html" target="_blank">
          <ButtonL class="w-10/12 sm:w-10/12 border-4 border-white">今すぐ無料相談はこちら</ButtonL>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
import ButtonL from '../CommonParts/ButtonL.vue'
import FirstviewPC from "@/assets/img/index/firstview/firstviewbg_PC.jpg"
import FirstviewSP from "@/assets/img/index/firstview/firstviewbg_SP.jpg"

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
  },
  methods: {
    handleScroll: function(evt, el) {
      console.log(window.scrollY);
      if (window.scrollY > 200) {
        el.setAttribute(
          "style",
          "opacity: 1; transform: translate3d(0, 0, 0)"
        );
      }
      // return window.scrollY > 600;
    },
    handleScroll2: function(evt, el) {
      console.log(window.scrollY);
      if (window.scrollY > 700) {
        el.setAttribute(
          "style",
          "opacity: 1; transform: translate3d(0, 0, 0)"
        );
      }
      // return window.scrollY > 800;
    }
  },
}
</script>

<style scoped>
@media screen and (max-width: 640px) {
	/* 640px以下に適用されるCSS（スマホ用） */
  .fv-bg{
    height:calc(100vh - 64px);
  }
}
/* .anim1{
  opacity: 0;
  transform: translate3d(0, 70px, 0);
  transition: 1.0s all cubic-bezier(0.39, 0.575, 0.565, 1);
} */
.anim1,.anim2,.anim3 {
  opacity: 0;
  animation-name: fadeUpAnime;/*アニメーションの定義名*/
  animation-fill-mode:forwards;/*アニメーションの開始・終了時の状態を指定*/
  animation-duration:2s;/*アニメーション１回分の時間の長さを指定*/
  animation-iteration-count:1;/*動きをループさせる回数*/
  animation-timing-function:ease;/*アニメーションの進行具合を操作*/
  animation-direction:normal;/*アニメーション再生の向き*/
}
.anim1{
  animation-delay: 0s;/*6で解説*/
}
.anim2{
  animation-delay: 0.4s;/*6で解説*/
}
.anim3{
  animation-delay: 0.5s;/*6で解説*/
}


/*1で解説*/
@keyframes fadeUpAnime{
  0% {
    opacity: 0;
    transform: translateY(100px);
  }

  100% {
    opacity: 1;
  }
}
</style>
