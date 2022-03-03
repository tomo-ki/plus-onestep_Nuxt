<template>
  <section id="charge" class="flex flex-col items-center w-full pt-10 pb-5 ms:py-16" style="background-color:#DBF2E8;">
  <h2 class="text-3xl font-bold mb-12">料金プラン</h2>
  <p class="w-9/10 sm:text-center">+one stepを利用するには、公式LINEアカウントの契約が必要です。</p>
  <div class="flex flex-col items-center bg-white w-10/12 py-10 mt-10" style="">
    <div class="mb-10">
      <img src="../assets/img/index/onestep/onestep_line.svg" alt="+one step" height="40px">
    </div>
    <div v-if="valOnestep==false" class="sm:hidden inline-block">
      <ButtonMplus @click="toggleOnestep()">料金プランを見る</ButtonMplus>
    </div>
    <div v-if="valOnestep==true" class="w-full overflow-x-scroll xl:overflow-x-visible flex justify-start sm:justify-center">
      <table class="border-separate text-center" width="95%" style="border-spacing: 4px 4px; white-space: nowrap;">
        <tr height="51">
          <td colspan="2" width="30%" class="mr-3"></td>
          <td rowspan="21" width="1%"></td>
          <th class="mx-5" width="30%" style="background-color:#D7EEEA;">MAプラン</th>
          <td rowspan="21" width="1%"></td>
          <th width="30%" style="background-color:#D7EEEA;">MA + 定着支援プラン</th>
        </tr>
        <tr>
          <td></td>
        </tr>
        <tr height="71">
          <th colspan="2" style="background-color:#D7EEEA;">初期費用</th>
          <td colspan="3">
            <span class="font-bold text-xl" style="color: #3AAEA7;">50,000円</span>
            <span>（初回契約時のみ）</span>
          </td>
        </tr>
        <tr>
          <td></td>
        </tr>
        <tr height="71">
          <th colspan="2" class="leading-4" style="background-color:#D7EEEA;">
            費用/月額
            <br>
            <span class="text-xs">
              ※12ヶ月契約
            </span>
          </th>
          <td class="font-bold text-xl" style="color: #3AAEA7;">30,000円</td>
          <td class="font-bold text-xl" style="color: #3AAEA7;">80,000円</td>
        </tr>
        <tr>
          <td></td>
        </tr>
        <tr height="71">
          <th colspan="2" style="background-color:#D7EEEA;">
            サポート内容
          </th>
          <td colspan="3">
            導入サポート、運用サポート、テンプレートプレゼント
          </td>
        </tr>
        <tr>
          <td></td>
        </tr>
        <tr height="39">
          <th rowspan="9" style="background-color:#D7EEEA;">機能<br>一覧</th>
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">自動タグ付け</th>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">予約配信機能</th>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">リマインダ機能</th>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">応募／購入スコアリング機能</th>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">CSVインポート</th>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">サーベイ機能</th>
          <td>ー</td>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">離職予兆機能</th>
          <td>ー</td>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">匿名相談機能</th>
          <td>ー</td>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#D7EEEA;">eNSP調査機能</th>
          <td>ー</td>
          <td class="text-xl font-bold" style="color:#3AAEA7;">〇</td>
        </tr>
        <tr>
          <td></td>
        </tr>
        <tr height="39">
          <th rowspan="3" style="background-color:#F3EBDD;">オプ<br>ション</th>
          <th class="text-sm font-normal" style="background-color:#F3EBDD;">オペレーター機能</th>
          <td>ー</td>
          <td>1,000円／アカウント</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#F3EBDD;">運用代行</th>
          <td>ー</td>
          <td>人数・内容によりお見積り</td>
        </tr>
        <tr height="39">
          <th class="text-sm font-normal" style="background-color:#F3EBDD;">課題コンサルティング・研修</th>
          <td>ー</td>
          <td>内容によりお見積り</td>
        </tr>
      </table>
    </div>
    <div v-if="valOnestep==true" class="mt-10 sm:hidden inline-block">
      <ButtonMminus @click="toggleOnestep()">閉じる</ButtonMminus>
    </div>
  </div>
  <div class="my-10">
    <img src="../assets/img/index/plus.svg" alt="">
  </div>
  <div class="flex flex-col items-center bg-white w-10/12 py-10">
    <div class="mb-10">
      <img src="../assets/img/index/LINEofficial.svg" alt="LINE公式アカウント">
    </div>
    <div v-if="valLINE==false" class="sm:hidden inline-block">
      <ButtonMplus @click="toggleLINE()">料金プランを見る</ButtonMplus>
    </div>
    <div v-if="valLINE==true" class="w-full overflow-x-scroll sm:overflow-x-visible flex justify-start sm:justify-center">
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
    <ButtonM>
      <router-link to="/contact.html" target="_blank">さらに詳しく知りたい方はこちら</router-link>
    </ButtonM>
  </div>
  </section>
</template>

<script>
import ButtonM from './CommonParts/ButtonM.vue'
import ButtonMplus from './CommonParts/ButtonMplus.vue'
import ButtonMminus from './CommonParts/ButtonMminus.vue'

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
</style>