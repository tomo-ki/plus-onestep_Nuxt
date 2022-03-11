<template>
  <div
    id="modalfeature"
    class="flex flex-col items-center pt-10 sm:justify-center"
    @click.self="$emit('close')"
  >
    <p>{{featureId}}</p>
    <div
      id="detailfeature"
      class="w-9/10 sm:w-8/12 overflow-y-scroll sm:overflow-visible"
      v-for="feature in features" :key="feature.id"
    >
      <div
        class="bg-white pt-20 pb-10 relative flex flex-col items-center"
        style="border:5px solid #B9E6D3;"
        v-if="feature.id == featureId"
      >
        <div class="w-9/10 sm:w-10/12 text-left">
          <h3 class="flex">
            <span class="text-6xl" style="color:#3AAEA7; font-family:Alternate Gothic No3 D;">
              {{ feature.id }}
            </span>
            <span class="text-2xl font-bold ml-4 pt-1">
              {{ feature.title }}
            </span>
          </h3>
        </div>
        <div class="w-9/10 sm:w-10/12 flex flex-col-reverse sm:flex-row items-center my-10">
          <div class="text-lg leading-9 w-9/10 sm:w-6/12 mt-6 sm:mr-10" style="min-height:280px;">
            <p>
              {{ feature.text1 }}
            </p>
            <p>
              {{ feature.text2 }}
            </p>
            <p>
              {{ feature.text3 }}
            </p>
            <p>
              {{ feature.text4 }}
            </p>
          </div>
          <div class="w-6/12 flex items-center justify-center sm:h-72">
            <img :src="feature.imgPath" :alt="feature.title" class="h-full">
          </div>
        </div>
        <div class="flex">
          <div class="cross">
            <img src="../../assets/img/index/common/cross.svg" alt="閉じる" @click="$emit('close')">
          </div>
          <div v-if="val>1" class="static sm:absolute top-1/2 left-0 sm:transform sm:-translate-y-1/2 sm:-translate-x-1/2 mr-6">
            <ButtonSL @click="toPrevious()" >前へ</ButtonSL>
          </div>
          <div v-if="val<6" class="sm:absolute top-1/2 right-0 sm:transform sm:-translate-y-1/2 sm:translate-x-1/2">
            <ButtonSR @click="toNext()">次へ</ButtonSR>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import ButtonSL from '../CommonParts/ButtonSL.vue'
import ButtonSR from '../CommonParts/ButtonSR.vue'

export default {
  name: 'ModalFeature',
  props: ['val'],
  components: {
    ButtonSL,
    ButtonSR
  },
  computed: {
    idid(){
      let id = this.val;
      return id;
    }
  },
  data(){
    return {
      featureId: null,
      features:[
        {
          "id":1,
          "title":'セグメント配信',
          "text1":'友だちの情報を「タグ」を使ってセグメント分けする機能です。',
          "text2":'性別や年齢の他に、部門、拠点、特徴などを設定できます。',
          "text3":'アンケート回収による自動タグ付け機能もあるので、効率的な運用が可能です。',
          "text4":'セグメント分けをすることで、個人を特定しピンポイントにメッセージを届けることが出来ます。',
          "imgPath":require('@/assets/img/index/feature/feature1.svg'),
        },
        {
          "id":2,
          "title":'応募・購買意欲のスコアリング',
          "text1":'WEBページにHTMLタグを埋め込むことで、いつ・誰が・どれくらいの時間、WEBページを訪れたか計測することが出来ますので応募・購買意欲のタイミングや、何に興味を持っているかが推測出来ます。',
          "text2":'頻度・回数などから意欲の高まりが数値化されるため、顧客へのピンポイント対応が可能になります。',
          "text3":' ',
          "text4":' ',
          "imgPath":require('@/assets/img/index/feature/feature2.svg'),
        },
        {
          "id":3,
          "title":'パルスサーベイ',
          "text1":'週1回のストレスチェックを実施することが出来ます。',
          "text2":'ストレスチェックの回答を集計し、傾向や推移を表示することで、気分の浮き沈み・悩みをひと目で確認することが出来るのでフォローが必要な従業員がわかります。',
          "text3":' ',
          "text4":' ',
          "imgPath":require('@/assets/img/index/feature/feature3.svg'),
        },
        {
          "id":4,
          "title":'離職予兆のスコアリング',
          "text1":'サーベイの結果や、コミュニケーション内容から離職傾向や予兆などのスコアリングが出来ます。',
          "text2":'優先的に対応すべき従業員が明確になり、効率化が図れます。',
          "text3":'職予兆者の早期発見に繋がります。',
          "text4":' ',
          "imgPath":require('@/assets/img/index/feature/feature4.svg'),
        },
        {
          "id":5,
          "title":'匿名相談・外部機関への相談',
          "text1":'プライバシーが守られた匿名での相談が出来るので、相談しにくい内容も抽出可能。',
          "text2":'また、弊社が第三者機関として相談窓口（別オプション）を設置しています。',
          "text3":' ',
          "text4":' ',
          "imgPath":require('@/assets/img/index/feature/feature5.svg'),
        },
        {
          "id":6,
          "title":'組織診断　eNPS調査',
          "text1":'eNPSとは「Employee Net Promoter Score」の略で、「自分が所属している会社を親しい友人や家族にどれくらい勧めたいか」という職場推奨度・職場へのロイヤリティーを可視化する世界的企業も導入している指標です。',
          "text2":'一般的にeNPSが高い企業は従業員の生産性や定着率が高いという傾向が示されるため、従業員の声を具体的に定量化することが出来ます。',
          "text3":'また、他業種のeNPSと比較することが出来るので自社の立ち位置が明確になります。',
          "text4":'',
          "imgPath":require('@/assets/img/index/feature/feature6.svg'),
        },
      ],
    }
  },
  methods: {
    getFeatureId(){
      this.featureId = this.val;
    },
    toPrevious(){
      // this.val -= 1;
      this.featureId-= 1;
    },
    toNext(){
      this.val += 1;
      this.featureId += 1;
    },
  },
  created() {
    this.getFeatureId();
  }
}
</script>
<style scoped>
#modalfeature{
  z-index:40;
  position:fixed;
  top:0;
  left:0;
  width:100%;
  height:100%;
  background-color:rgba(0, 0, 0, 0.2);
}
.cross{
  position: absolute;
  top: 15px;
  right: 15px;
  cursor: pointer;
}
.cross:hover{
  opacity: 0.5;
}
</style>
