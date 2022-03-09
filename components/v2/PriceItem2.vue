<template>
  <section id="price" class="flex flex-col items-center w-full pb-5 ms:py-16" style="background-color:#DBF2E8;">
  <div class="w-full flex justify-center items-center h-20 sm:h-24" style="background-color:#3AAEA7;">
    <h2 class="text-2xl sm:text-3xl font-bold text-white">料金プラン</h2>
  </div>
  <p class="mt-10 w-9/10 sm:text-center">+one stepを利用するには、公式LINEアカウントの契約が必要です。</p>
  <div class="flex flex-col items-center bg-white w-11/12 sm:w-9/12 py-10 mt-10 shadow-lg" style="border:solid 5px #9CD8D4;">
    <div class="mb-10">
      <img src="../../assets/img/index/onestep/onestep_line.png" alt="+one step" class="h-10">
    </div>
    <div v-if="valOnestep==false" class="sm:hidden inline-block">
      <ButtonMplus @click="toggleOnestep()">料金プランを見る</ButtonMplus>
    </div>
    <div v-if="valOnestep==true" class="w-full overflow-x-scroll xl:overflow-x-visible flex justify-start sm:justify-center">
      <table class="border-separate text-center" width="95%" style="border-spacing: 4px 4px; white-space: nowrap;">
        <colgroup span="2" class="Title"></colgroup>
        <colgroup span="1" class="Margin1"></colgroup>
        <colgroup span="1" class="MA"></colgroup>
        <colgroup span="1" class="Margin2"></colgroup>
        <colgroup span="1" class="MAplus"></colgroup>


        <tr>
          <td colspan="2" width="30%" class="mr-3"></td>
          <td rowspan="22" width="1%"></td>
          <td></td>
          <td rowspan="22" width="1%"></td>
          <th rowspan="2" width="30%" style="background-color:#FFE88A;" valign="bottom" class="pb-7 pt-3 rounded-t-xl th-MAplus">
            <div class="flex flex-col items-center">
              <img src="../../assets/img/index/charge/charge_v2_MAplus.png" alt="" class="">
              <h3 class="text-2xl my-3">
                MA + 定着支援プラン
              </h3>
              <p class="text-center font-normal text-sm">
                「職場でいつ、どこで、何が」
                <br>
                「従業員のコンディション」
                <br>
                「エンゲージメント」を可視化したいなら
              </p>
            </div>
          </th>
        </tr>
        <tr>
          <td></td>
          <td></td>
          <th class="mx-5 py-7 rounded-t-xl" width="30%" height="60px" style="background-color:#D7EEEA;" valign="bottom">
            <div class="flex flex-col items-center">
              <img src="../../assets/img/index/charge/charge_v2_MA.png" alt="" class="w-6/12">
              <h3 class="text-2xl my-3">
                MAプラン
              </h3>
              <p class="text-center font-normal text-sm">
                潜在顧客へのアプローチを
                <br>
                自動化したいなら
              </p>
            </div>
          </th>
        </tr>
        <tr>
          <td></td>
          <td></td>
          <td></td>
        </tr>
        <tr height="71">
          <th colspan="2" style="background-color:#D7EEEA;">
            <div class="flex ml-7">
              <img src="../../assets/img/index/charge/charge_v2_icon1.svg" alt="">
              <p class="ml-5">初期費用</p>
            </div>
          </th>
          <td>
            <span class="font-bold text-xl" style="color: #3AAEA7;">50,000円</span>
            <span>（初回契約時のみ）</span>
          </td>
          <td>
            <span class="font-bold text-xl" style="color: #3AAEA7;">50,000円</span>
            <span>（初回契約時のみ）</span>
          </td>
        </tr>
        <tr>
        </tr>
        <tr height="71">
          <th colspan="2" style="background-color:#D7EEEA;">
            <div class="flex ml-7">
              <img src="../../assets/img/index/charge/charge_v2_icon2.svg" alt="">
              <p class="ml-5">
                費用/月額
                <span class="text-xs">
                  ※12ヶ月契約
                </span>
              </p>
            </div>
          </th>
          <td class="font-bold text-2xl" style="color: #3AAEA7;">30,000円</td>
          <td class="font-bold text-2xl" style="color: #3AAEA7;">80,000円</td>
        </tr>
        <tr>
          <td></td>
        </tr>
        <tr height="71">
          <th colspan="2" style="background-color:#D7EEEA;">
            <div class="flex ml-7">
              <img src="../../assets/img/index/charge/charge_v2_icon3.svg" alt="">
              <p class="ml-5">
                サポート内容
              </p>
            </div>
          </th>
          <td>
            導入サポート、運用サポート、
            <br>
            テンプレートプレゼント
          </td>
          <td>
            導入サポート、運用サポート、
            <br>
            テンプレートプレゼント
          </td>
        </tr>
        <tr>
          <td></td>
        </tr>
        <tr height="39">
          <th rowspan="9" style="background-color:#D7EEEA;">
            <div class="flex flex-col items-center">
              <img src="../../assets/img/index/charge/charge_v2_icon4.svg" alt="">
              <p class="mt-3">
                機能
                <br>
                一覧
              </p>
            </div>
          </th>
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">自動タグ付け</th>
          <td class="text-xl font-bold" style="color:#3AAEA7;">◎</td>
          <td class="text-xl font-bold z-10" style="color: #3AAEA7; background-color:#FFF7D8;">◎</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">予約配信機能</th>
          <td class="text-xl font-bold" style="color:#3AAEA7;">◎</td>
          <td class="text-xl font-bold" style="color: #3AAEA7; background-color:#FFF7D8;">◎</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">リマインダ機能</th>
          <td class="text-xl font-bold" style="color:#3AAEA7;">◎</td>
          <td class="text-xl font-bold" style="color: #3AAEA7; background-color:#FFF7D8;">◎</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">応募／購入スコアリング機能</th>
          <td class="text-xl font-bold" style="color:#3AAEA7;">◎</td>
          <td class="text-xl font-bold" style="color: #3AAEA7; background-color:#FFF7D8;">◎</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">CSVインポート</th>
          <td class="text-xl font-bold" style="color:#3AAEA7;">◎</td>
          <td class="text-xl font-bold" style="color: #3AAEA7; background-color:#FFF7D8;">◎</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">サーベイ機能</th>
          <td>ー</td>
          <td class="text-xl font-bold" style="color: #3AAEA7; background-color:#FFF7D8;">◎</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">離職予兆機能</th>
          <td>ー</td>
          <td class="text-xl font-bold" style="color: #3AAEA7; background-color:#FFF7D8;">◎</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">匿名相談機能</th>
          <td>ー</td>
          <td class="text-xl font-bold" style="color: #3AAEA7; background-color:#FFF7D8;">◎</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">eNSP調査機能</th>
          <td>ー</td>
          <td class="text-xl font-bold" style="color: #3AAEA7; background-color:#FFF7D8;">◎</td>
        </tr>
        <tr>
          <td></td>
        </tr>
        <tr height="39">
          <th rowspan="3" style="background-color:#E5DCFF;">
            <div class="flex flex-col items-center">
              <img src="../../assets/img/index/charge/charge_v2_icon4.svg" alt="">
              <p class="mt-3">
                オプ
                <br>
                ション
              </p>
            </div>
          </th>
          <th class="text-sm font-normal" style="background-color:#E5DCFF;">オペレーター機能</th>
          <td>ー</td>
          <td style="background-color:#FFF7D8;">1,000円／アカウント</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#E5DCFF;">運用代行</th>
          <td>ー</td>
          <td>人数・内容によりお見積り</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#E5DCFF;">課題コンサルティング・研修</th>
          <td>ー</td>
          <td>内容によりお見積り</td>
        </tr>
      </table>
    </div>
    <div v-if="valOnestep==true" class="mt-10 sm:hidden inline-block">
      <ButtonMminus @click="toggleOnestep()">閉じる</ButtonMminus>
    </div>
  </div>
  <!--  -->
  <div class="my-10">
    <img src="../../assets/img/index/price/plus.png" alt="" class="h-10">
  </div>
  <!--  -->
  <!-- LINE -->
  <div class="flex flex-col items-center bg-white w-11/12 sm:w-9/12 py-10 shadow-lg" style="border:solid 5px #C0F1A4;">
    <div class="mb-10">
      <img src="../../assets/img/index/price/LINEofficial.png" alt="LINE公式アカウント" class="h-8">
    </div>
    <div v-if="valLINE==false" class="sm:hidden inline-block">
      <ButtonMplus @click="toggleLINE()">料金プランを見る</ButtonMplus>
    </div>
    <div v-if="valLINE==true" class="w-full overflow-x-scroll xl:overflow-x-visible flex justify-start sm:justify-center">
      <table class="border-separate text-center" width="95%" style="border-spacing: 5px 3px; white-space: nowrap;">
        <tr height="51">
          <td class="px-10" width="30%"></td>
          <td rowspan="6" width="1%"></td>
          <th class="px-10" width="20%" style="background-color:#C0F1A4;">フリープラン</th>
          <td rowspan="6" width="1%"></td>
          <th class="px-10" width="20%" style="background-color:#C0F1A4;">ライトプラン</th>
          <td rowspan="6" width="1%"></td>
          <th class="px-3" width="20%" style="background-color:#C0F1A4;">スタンダードプラン</th>
        </tr>
        <tr height="51">
          <th style="background-color:#C0F1A4;">月額固定</th>
          <td>無料</td>
          <td>5,000円</td>
          <td>15,000円</td>
        </tr>
        <tr>
          <td></td>
        </tr>
        <tr height="51">
          <th style="background-color:#C0F1A4;">無料メッセージ通数</th>
          <td>1,000通</td>
          <td>15,000通</td>
          <td>45,000通</td>
        </tr>
        <tr>
          <td></td>
        </tr>
        <tr height="51">
          <th style="background-color:#C0F1A4;">追加メッセージ</th>
          <td>不可</td>
          <td>5円</td>
          <td>〜3円</td>
        </tr>
      </table>
    </div>
    <div v-if="valLINE==true" class="mt-10 sm:hidden inline-block">
      <ButtonMminus @click="toggleLINE()">閉じる</ButtonMminus>
    </div>
  </div>
  <div class="w-10/12 text-center sm:text-right py-3">
    <p class="text-sm">※金額は全て税抜き</p>
  </div>
  <div class="my-10">
    <a href="/contact.html" target="_blank">
      <ButtonM>さらに詳しく知りたい方はこちら</ButtonM>
    </a>
  </div>
  </section>
</template>

<script>
import ButtonM from '../CommonParts/ButtonM.vue'
import ButtonMplus from '../CommonParts/ButtonMplus.vue'
import ButtonMminus from '../CommonParts/ButtonMminus.vue'

export default {
  name: 'Charge',
  components: {
    ButtonM,
    ButtonMplus,
    ButtonMminus,
  },
  data(){
    return {
      valOnestep:false,
      valLINE:false,
    }
  },
  methods: {
    getOnestep(){
      if(window.innerWidth >= 640){
        this.valOnestep = true;
      }else{
        this.valOnestep = false;
      }
    },
    toggleOnestep(){
      if(this.valOnestep == false){
        this.valOnestep = true;
      }else{
        this.valOnestep = false;
      }
    },
    getLINE(){
      if(window.innerWidth >= 640){
        this.valLINE = true;
      }else{
        this.valLINE = false;
      }
    },
    toggleLINE(){
      if(this.valLINE == false){
        this.valLINE = true;
      }else{
        this.valLINE = false;
      }
    },
  },
  created(){
    this.getOnestep();
    this.getLINE();
  }
}
</script>

<style scoped>
th{
  font-size:16px;
}
td{
  border-bottom: 1px solid #707070;
  empty-cells:hide;
}
.MAplus{
  background-color: #FFF7D8;
}
.th-MAplus{
  position: relative;
}
/* .th-MAplus:after{
  content: "";
  position: absolute;
  width: 100%;
  height: 768px;
  background-color: #FFF7D8;
  bottom: 0;
  left: 0;
  transform: translate(0, 100%);

} */
</style>