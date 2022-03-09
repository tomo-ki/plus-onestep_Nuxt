<template>
  <div id="home">
    <main>
      <HeaderItem/>
      <TopItem/>
      <AboutItem/>
      <MeritItem/>
      <FlowItem/>
      <FeatureItem/>
      <ChargeItem/>
      <FaqItem/>
      <Banner class="sm:hidden block"/>
      <FooterItem/>
    </main>
  </div>
</template>

<script>
import HeaderItem from '@/components/HeaderItem.vue'
import TopItem from '~/components/v2/TopItem.vue'
import AboutItem from '~/components/v2/AboutItem.vue'
import MeritItem from '~/components/v1/MeritItem.vue'
import FlowItem from '@/components/v2/FlowItem.vue'
import FeatureItem from '@/components/v2/FeatureItem.vue'
import ChargeItem from '~/components/v2/PriceItem2.vue'
import FaqItem from '@/components/v2/FaqItem.vue'
import Banner from '~/components/v1/Banner1.vue'
import FooterItem from '@/components/FooterItem.vue'


export default {
  name: 'Home',
  components: {
    HeaderItem,
    TopItem,
    AboutItem,
    MeritItem,
    FlowItem,
    FeatureItem,
    ChargeItem,
    FaqItem,
    Banner,
    FooterItem,
  },
  data(){
    return {
    }
  }
}
</script>

