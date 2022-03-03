<template>
  <div id="home">
    <main>
      <HeaderItem/>
      <TopItem/>
      <AboutItem/>
      <MeritItem/>
      <FeatureItem/>
      <ChargeItem/>
      <Banner1 class="sm:hidden block"/>
      <FooterItem/>
    </main>
  </div>
</template>

<script>
import HeaderItem from '../components/HeaderItem.vue'
import TopItem from '../components/TopItem.vue'
import AboutItem from '@/components/AboutItem.vue'
import MeritItem from '@/components/MeritItem.vue'
import FeatureItem from '@/components/FeatureItem.vue'
import ChargeItem from '@/components/ChargeItem.vue'
import Banner1 from '@/components/Banner1.vue'
import FooterItem from '@/components/FooterItem.vue'


export default {
  name: 'Home',
  components: {
    HeaderItem,
    TopItem,
    AboutItem,
    MeritItem,
    FeatureItem,
    ChargeItem,
    Banner1,
    FooterItem,
  },
  data(){
    return {
    }
  }
}
</script>

