<template>
  <section id="merit" class="flex flex-col items-center overflow-hidden py-20" style="background-color:#DBF2E8;">
    <div>
      <h2 class="text-3xl">
        <span style="color:#3AAEA7; font-family:Alternate Gothic No3 D;" class="text-6xl sm:text-7xl">
          3
        </span>
        <span class="font-bold text-2xl sm:text-3xl">
          つの導入メリット
        </span>
      </h2>
    </div>
    <div class="sm:flex sm:justify-between mt-10 mb-0 w-9/10 sm:w-11/12">
      <div
        class="ribbon merit1 text-center bg-white p-10 pb-28 mb-24 sm:w-3/10"
        style="border:5px solid #BBA2FF; border-bottom:none;"
      >
        <div
          style="color:#BBA2FF; font-family:Alternate Gothic No3 D;"
          class="text-6xl"
        >
          1
        </div>
        <h3 class="mb-7">
          <span class="font-bold leading-8 text-xl" style="background: linear-gradient(transparent 80%, #D0BFFF 30%);">
            過去に繋がりのあった
          </span>
            <br>
          <span class="font-bold leading-8 text-xl" style="background: linear-gradient(transparent 80%, #D0BFFF 30%);">
            顧客のコミュニティ形成
          </span>
        </h3>
        <p class="text-left text-sm leading-6">
          公式LINEアカウントを活用して、これまで成約には至らなかったが繋がりのあった顧客のコミュニティを形成することが可能です。新規で広告を出すよりも、潜在顧客としてコスト効率よく効果的なアプローチが実現します。
        </p>
        <span class="linehider"></span>
        <img class="meritimg" src="../../assets/img/index/merit/merit1.svg" alt="">
      </div>
      <div
        class="ribbon merit2 text-center bg-white p-10 pb-28 mb-24 sm:w-3/10"
        style="border:5px solid #81CFE3; border-bottom:none;"
      >
        <div
          style="color:#81CFE3; font-family:Alternate Gothic No3 D;"
          class="text-6xl"
        >
          2
        </div>
        <h3 class="mb-7">
          <span class="font-bold leading-8 text-xl" style="background: linear-gradient(transparent 80%, #81CFE3 30%);">
            顧客との
          </span>
            <br>
          <span class="font-bold leading-8 text-xl" style="background: linear-gradient(transparent 80%, #81CFE3 30%);">
            コミュニケーション活性化
          </span>
        </h3>
        <p class="text-left text-sm leading-6">
          到達率や開封率の高い生活インフラであるLINEを使ったツールのため、ストレスフリーで活用できます。一斉配信だけでなく、個別チャットもでき、画像送付など、視覚的に訴えることで反応率UPに繋がり、効果的なコミュニケーションが可能になります。
        </p>
        <span class="linehider"></span>
        <img class="meritimg" src="../../assets/img/index/merit/merit2.svg" alt="">
      </div>
      <div
        class="ribbon merit3 text-center bg-white p-10 pb-28 mb-24 sm:w-3/10"
        style="border:5px solid #FFDD54; border-bottom:none;"
      >
        <div
          style="color:#FFDD54; font-family:Alternate Gothic No3 D;"
          class="text-6xl"
        >
          3
        </div>
        <h3 class="mb-7 h-16 pt-4">
          <span class="font-bold leading-8 text-xl" style="background: linear-gradient(transparent 80%, #FFDD54 30%);">
            従業員の定着率向上
          </span>
        </h3>
        <p class="text-left text-sm leading-6">
          従業員の早期離職は時間やコストの大きな損失です。+ one stepでは、入社したその日から、モチベーション管理、定期アンケート、メンタルケアなどを運用することができるため、離職予兆を見逃さず、先手のフォローが可能です。多くの会社で定着率が向上しています。
        </p>
        <span class="linehider"></span>
        <img class="meritimg" src="../../assets/img/index/merit/merit3.svg" alt="">
      </div>
    </div>
  </section>
</template>

<script>
import Merit1Svg from "@/assets/img/index/merit/merit1.svg"
import Merit2Svg from "@/assets/img/index/merit/merit2.svg"
import Merit3Svg from "@/assets/img/index/merit/merit3.svg"


export default {
  name: 'Merit',
  components: {
  },
  data(){
    return {
      Merit1: Merit1Svg,
      Merit2: Merit2Svg,
      Merit3: Merit3Svg,
    }
  }
}
</script>
<style scoped>
.ribbon{
  position: relative;
}
.ribbon:before, .ribbon:after{
  content: "";
  position:absolute;
  bottom: 0;
  left:-4vw;
  width:0;
  height:0;
  border-style: solid;
  border-width: 0px 48vw 60px;
}
.ribbon:after{
  bottom: -5px;
  border-color: transparent transparent #DBF2E8 transparent;
  -webkit-filter:drop-shadow(2px 2px 2px rgba(0,0,0,0.5) inset);
  /* border-color: transparent transparent transparent transparent; */
  box-shadow:0px 8px 8px -1px rgb(179, 179, 179) inset;
}
.merit1:before{
  border-color: transparent transparent #BBA2FF transparent;
}
.merit2:before{
  border-color: transparent transparent #81CFE3 transparent;
}
.merit3:before{
  border-color: transparent transparent #FFDD54 transparent;
}
.linehider:before, .linehider:after{
  content: "";
  position:absolute;
  bottom: -10px;
  width:30px;
  height:30px;
  background-color: #DBF2E8;
}
.linehider:before{
  left:-35px;
}
.linehider:after{
  right: -35px;
}
.meritimg{
  position:absolute;
  z-index: 5;
  bottom: -70px;
  left: 50%;
  transform: translate(-50%, 0);
}
@media screen and (min-width: 640px) {
  .ribbon:before, .ribbon:after{
    left:-1.8vw;
    border-width: 0px 15vw 60px;
  }
}
</style>