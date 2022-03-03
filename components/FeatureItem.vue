<template>
  <section id="feature" class="flex flex-col items-center w-full py-16">
    <h2 class="flex items-center mb-14 sm:mb-16">
      <img src="../assets/img/index/onestep/onestep_line.svg" alt="+one step">
      <span class="text-2xl sm:text-3xl font-bold ml-4">
        でできること
      </span>
    </h2>
    <div class="w-9/10 sm:w-11/12 flex flex-col items-center sm:flex-row sm:flex-wrap justify-between">
      <div
        v-for="feature in features" :key="feature.id"
        class="p-8 mb-10 sm:mb-6 shadow-lg w-full sm:w-49/100 relative"
        style="border:solid 5px #B9E6D3; "
      >
        <h3 class="flex">
          <span class="text-6xl" style="color:#3AAEA7; font-family:Alternate Gothic No3 D;">
            {{ feature.id }}
          </span>
          <span class="text-xl sm:text-2xl font-bold ml-4 sm:pt-1">
            {{ feature.title }}
          </span>
        </h3>
        <div class="flex flex-col items-center sm:flex-row sm:justify-between">
          <div class="flex flex-col justify-between sm:w-7/12">
            <p class="text-base pb-6 leading-7">
              {{ feature.text1 }}
              <br class="hidden lg:inline-block">
              {{ feature.text2 }}
            </p>
            <div class="absolute bottom-0 left-1/2 transform translate-y-1/2 -translate-x-1/2 sm:static sm:transform-none">
              <ButtonSR @click="openModal(feature.id)">詳しく見る</ButtonSR>
            </div>
          </div>
          <div class="flex items-end justify-center w-6/12">
            <img :src="feature.imgPath" :alt="feature.title" class="h-36">
          </div>
        </div>
        <Modal :val="postId" v-show="showContent" @close="closeModal()"/>
      </div>
    </div>
    <div class="px-4 my-10">
      <ButtonM><router-link to="/contact.html" target="_blank">さらに詳しく知りたい方はこちら</router-link></ButtonM>
    </div>
  </section>
</template>


<script>
import ButtonM from './CommonParts/ButtonM.vue'
import ButtonSR from './CommonParts/ButtonSR.vue'
import Modal from './ModalFeature.vue'

export default {
  name: 'Feature',
  components: {
    ButtonM,
    ButtonSR,
    Modal,
  },
  data(){
    return {
      showContent: false,
      postId: "",
      features:[
        {
          "id":1,
          "title":'セグメント配信',
          "text1":'友だちの情報を「タグ」を',
          "text2":'使ってセグメント分け',
          "imgPath":require('@/assets/img/index/feature/feature1.png'),
        },
        {
          "id":2,
          "title":'応募・購買意欲のスコアリング',
          "text1":'WEBページにHTMLタグを',
          "text2":'埋め込み、様々な情報を計測',
          "imgPath":require('@/assets/img/index/feature/feature2.png'),
        },
        {
          "id":3,
          "title":'パルスサーベイ',
          "text1":'週1回のストレスチェックを',
          "text2":'実施・集計',
          "imgPath":require('@/assets/img/index/feature/feature3.png'),
        },
        {
          "id":4,
          "title":'離職予兆のスコアリング',
          "text1":'離職傾向や予兆などを',
          "text2":'スコアリング',
          "imgPath":require('@/assets/img/index/feature/feature4.png'),
        },
        {
          "id":5,
          "title":'匿名相談・外部機関への相談',
          "text1":'プライバシーが守られた',
          "text2":'匿名での相談',
          "imgPath":require('@/assets/img/index/feature/feature5.png'),
        },
        {
          "id":6,
          "title":'組織診断　eNPS調査',
          "text1":'職場推奨度・職場への',
          "text2":'ロイヤリティーを可視化',
          "imgPath":require('@/assets/img/index/feature/feature6.png'),
        },
      ],
    }
  },
  methods: {
    openModal(featureId) {
      this.showContent = true
      this.postId = featureId
    },
    closeModal () {
      this.showContent = false
    }
  }
}
</script>