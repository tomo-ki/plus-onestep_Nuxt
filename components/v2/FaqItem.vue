<template>
  <section id="faq" class="flex flex-col items-center my-10 w-full">
    <div class="flex justify-center py w-10/12">
      <img src="../../assets/img/index/faq/faq_v2_img1.svg" alt="">
      <h2 class="text-2xl sm:text-3xl font-bold py-16 w-7/12">
        よくあるご質問 Q&A
      </h2>
    </div>
    <div class="w-10/12 flex flex-col items-center">
      <!-- FAQ no1 -->
      <div
        v-if="valQa1==false"
        @click="toggleQa1()"
        class="flex items-center py-2 shadow-lg mb-5 sm:mb-10 q-open w-full max-w-screen-lg" style="border:solid 5px #B9E6D3;"
      >
        <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
          <img src="../../assets/img/index/faq/faq_v2_Q.png" alt="Q" class="w-4 sm:w-6">
        </div>
        <div class="flex items-center justify-between w-10/12 sm:w-11/12 pr-3">
          <p class="text-base sm:text-2xl">
            デモ画面はありますか？
          </p>
          <img src="../../assets/img/index/faq/faq_v2_down.svg" alt="Q" width="15px">
        </div>
      </div>
      <div
        v-if="valQa1==true"
        style="border:solid 5px #B9E6D3;"
        class="shadow-lg mb-5 sm:mb-10 w-full max-w-screen-lg"
      >
        <div @click="toggleQa1()" class="flex items-center py-2 q-close" style="background-color: #DAF5EA;">
          <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
          <img src="../../assets/img/index/faq/faq_v2_Q.png" alt="Q" class="w-4 sm:w-6">
        </div>
        <div class="flex items-center justify-between w-10/12 sm:w-11/12 pr-3">
            <p class="text-base sm:text-2xl">
              デモ画面はありますか？
            </p>
            <img src="../../assets/img/index/faq/faq_v2_up.svg" alt="" width="15px">
          </div>
        </div>
        <div class="flex py-2">
          <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
            <img src="../../assets/img/index/faq/faq_v2_A.png" alt="A" class="w-4 sm:w-6" width="">
          </div>
          <div class="w-10/12 sm:w-11/12 text-base sm:text-lg py-4 pr-4 leading-8">
            <p>
              無料で利用できるデモ画面を準備させていただきます。利用期間は1週間になります。
            </p>
          </div>
        </div>
      </div>
      <!-- FAQ no2 -->
      <div
        v-if="valQa2==false"
        @click="toggleQa2()"
        class="flex items-center py-2 shadow-lg mb-5 sm:mb-10 q-open w-full max-w-screen-lg" style="border:solid 5px #B9E6D3;"
      >
        <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
          <img src="../../assets/img/index/faq/faq_v2_Q.png" alt="Q" class="w-4 sm:w-6">
        </div>
        <div class="flex items-center justify-between w-10/12 sm:w-11/12 pr-3">
          <p class="text-base sm:text-2xl">
            契約期間中でもプラン変更は出来ますか？
          </p>
          <img src="../../assets/img/index/faq/faq_v2_down.svg" alt="" width="15px">
        </div>
      </div>
      <div
        v-if="valQa2==true"
        style="border:solid 5px #B9E6D3;"
        class="shadow-lg mb-5 sm:mb-10 w-full max-w-screen-lg"
      >
        <div @click="toggleQa2()" class="flex items-center py-2 q-close" style="background-color: #DAF5EA;">
          <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
          <img src="../../assets/img/index/faq/faq_v2_Q.png" alt="Q" class="w-4 sm:w-6">
        </div>
        <div class="flex items-center justify-between w-10/12 sm:w-11/12 pr-3">
            <p class="text-base sm:text-2xl">
              契約期間中でもプラン変更は出来ますか？
            </p>
            <img src="../../assets/img/index/faq/faq_v2_up.svg" alt="" width="15px">
          </div>
        </div>
        <div class="flex py-2">
          <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
            <img src="../../assets/img/index/faq/faq_v2_A.png" alt="A" class="w-4 sm:w-6" width="">
          </div>
          <div class="w-10/12 sm:w-11/12 text-base sm:text-lg py-4 pr-4 leading-8">
            <p>
              MAプランから定着支援プランへの変更は出来ます。ただし、MA+定着支援プランからMAプランへの変更は出来ません。
            </p>
          </div>
        </div>
      </div>
      <!-- FAQ no3 -->
      <div
        v-if="valQa3==false"
        @click="toggleQa3()"
        class="flex items-center py-2 shadow-lg mb-5 sm:mb-10 q-open w-full max-w-screen-lg" style="border:solid 5px #B9E6D3;"
      >
        <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
          <img src="../../assets/img/index/faq/faq_v2_Q.png" alt="Q" class="w-4 sm:w-6">
        </div>
        <div class="flex items-center justify-between w-10/12 sm:w-11/12 pr-3">
          <p class="text-base sm:text-2xl">
            +onestepの動作環境をおしえてください
          </p>
          <img src="../../assets/img/index/faq/faq_v2_down.svg" alt="" width="15px">
        </div>
      </div>
      <div
        v-if="valQa3==true"
        style="border:solid 5px #B9E6D3;"
        class="shadow-lg mb-5 sm:mb-10 w-full max-w-screen-lg"
      >
        <div @click="toggleQa3()" class="flex items-center py-2 q-close" style="background-color: #DAF5EA;">
          <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
          <img src="../../assets/img/index/faq/faq_v2_Q.png" alt="Q" class="w-4 sm:w-6">
        </div>
        <div class="flex items-center justify-between w-10/12 sm:w-11/12 pr-3">
            <p class="text-base sm:text-2xl">
              +onestepの動作環境をおしえてください
            </p>
            <img src="../../assets/img/index/faq/faq_v2_up.svg" alt="" width="15px">
          </div>
        </div>
        <div class="flex py-2">
          <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
            <img src="../../assets/img/index/faq/faq_v2_A.png" alt="A" class="w-4 sm:w-6" width="">
          </div>
          <div class="w-10/12 sm:w-11/12 text-base sm:text-lg py-4 pr-4 leading-8">
            <p>
              1. Windows の場合
              <br>
                <span class="inline-block w-3"></span>・Windows 8, Windows 10で動作します。
              <br>
                <span class="inline-block w-3"></span>・Microsoft Edge最新版
              <br>
                <span class="inline-block w-3"></span>・Mozilla Firefox最新版
              <br>
                <span class="inline-block w-3"></span>・Google Chrome最新版
              <br>
              2. Mac OSの場合
              <br>
                <span class="inline-block w-3"></span>・Mac OS（最新版の1世代前まで）で動作します。
              <br>
                <span class="inline-block w-3"></span>・Apple Safari最新版
              <br>
                <span class="inline-block w-3"></span>・Mozilla Firefox最新版
              <br>
                <span class="inline-block w-3"></span>・Google Chrome最新版
              <br>
            </p>
          </div>
        </div>
      </div>
      <!-- FAQ no4 -->
      <div
        v-if="valQa4==false"
        @click="toggleQa4()"
        class="flex items-center py-2 shadow-lg mb-5 sm:mb-10 q-open w-full max-w-screen-lg" style="border:solid 5px #B9E6D3;"
      >
        <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
          <img src="../../assets/img/index/faq/faq_v2_Q.png" alt="Q" class="w-4 sm:w-6">
        </div>
        <div class="flex items-center justify-between w-10/12 sm:w-11/12 pr-3">
          <p class="text-base sm:text-2xl">
            LINE以外にメッセージ配信出来ますか？
          </p>
          <img src="../../assets/img/index/faq/faq_v2_down.svg" alt="" width="15px">
        </div>
      </div>
      <div
        v-if="valQa4==true"
        style="border:solid 5px #B9E6D3;"
        class="shadow-lg mb-5 sm:mb-10 w-full max-w-screen-lg"
      >
        <div @click="toggleQa4()" class="flex items-center py-2 q-close" style="background-color: #DAF5EA;">
          <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
          <img src="../../assets/img/index/faq/faq_v2_Q.png" alt="Q" class="w-4 sm:w-6">
        </div>
        <div class="flex items-center justify-between w-10/12 sm:w-11/12 pr-3">
            <p class="text-base sm:text-2xl">
              LINE以外にメッセージ配信出来ますか？
            </p>
            <img src="../../assets/img/index/faq/faq_v2_up.svg" alt="" width="15px">
          </div>
        </div>
        <div class="flex py-2">
          <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
            <img src="../../assets/img/index/faq/faq_v2_A.png" alt="A" class="w-4 sm:w-6" width="">
          </div>
          <div class="w-10/12 sm:w-11/12 text-base sm:text-lg py-4 pr-4 leading-8">
            <p>
              メール配信も可能です。
            </p>
          </div>
        </div>
      </div>
      <!-- FAQ no5 -->
      <div
        v-if="valQa5==false"
        @click="toggleQa5()"
        class="flex items-center py-2 shadow-lg mb-5 sm:mb-10 q-open w-full max-w-screen-lg" style="border:solid 5px #B9E6D3;"
      >
        <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
          <img src="../../assets/img/index/faq/faq_v2_Q.png" alt="Q" class="w-4 sm:w-6">
        </div>
        <div class="flex items-center justify-between w-10/12 sm:w-11/12 pr-3">
          <p class="text-base sm:text-2xl">
            セキュリティは大丈夫ですか？
          </p>
          <img src="../../assets/img/index/faq/faq_v2_down.svg" alt="" width="15px">
        </div>
      </div>
      <div
        v-if="valQa5==true"
        style="border:solid 5px #B9E6D3;"
        class="shadow-lg mb-5 sm:mb-10 w-full max-w-screen-lg"
      >
        <div @click="toggleQa5()" class="flex items-center py-2 q-close" style="background-color: #DAF5EA;">
          <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
          <img src="../../assets/img/index/faq/faq_v2_Q.png" alt="Q" class="w-4 sm:w-6">
        </div>
        <div class="flex items-center justify-between w-10/12 sm:w-11/12 pr-3">
            <p class="text-base sm:text-2xl">
              セキュリティは大丈夫ですか？
            </p>
            <img src="../../assets/img/index/faq/faq_v2_up.svg" alt="" width="15px">
          </div>
        </div>
        <div class="flex py-2">
          <div class="w-2/12 sm:w-1/12 flex flex-col items-center mt-3">
            <img src="../../assets/img/index/faq/faq_v2_A.png" alt="A" class="w-4 sm:w-6" width="">
          </div>
          <div class="w-10/12 sm:w-11/12 text-base sm:text-lg py-4 pr-4 leading-8">
            <p>
              負荷に強いAWSをサーバーに採用し、IPアクセス制限や二段階認証を行うことで強固なセキュリティ対策を行なっております。
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>


export default {
  name: 'Faq',
  components: {
  },
  data(){
    return {
      valQa1: false,
      valQa2: false,
      valQa3: false,
      valQa4: false,
      valQa5: false,
      faqs:[
        {
          "id":1,
          "question":'セグメント配信',
          "answer":'友だちの情報を「タグ」を使ってセグメント分け',
          "valFaq":false,
        },
      ]
    }
  },
  methods: {
    toggleFaq(){
      if(this.valQa1==false){
        this.valQa1=true;
      }
      else{
        this.valQa1=false;
      }
    },
    toggleQa1(){
      if(this.valQa1==false){
        this.valQa1=true;
      }
      else{
        this.valQa1=false;
      }
    },
    toggleQa2(){
      if(this.valQa2==false){
        this.valQa2=true;
      }
      else{
        this.valQa2=false;
      }
    },
    toggleQa3(){
      if(this.valQa3==false){
        this.valQa3=true;
      }
      else{
        this.valQa3=false;
      }
    },
    toggleQa4(){
      if(this.valQa4==false){
        this.valQa4=true;
      }
      else{
        this.valQa4=false;
      }
    },
    toggleQa5(){
      if(this.valQa5==false){
        this.valQa5=true;
      }
      else{
        this.valQa5=false;
      }
    },
  },
}
</script>

<style scoped>
.q-open:hover{
  background-color: #DAF5EA;
  cursor: pointer;
}
.q-close:hover{
  background-color: #DAF5EA;
  cursor: pointer;
}
</style>