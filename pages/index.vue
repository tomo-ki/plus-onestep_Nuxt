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
export default {
  name: 'Home',
  components: {
    HeaderItem:()=>import('@/components/HeaderItem.vue'),
    TopItem:()=>import('@/components/v2/TopItem.vue'),
    AboutItem:()=>import('@/components/v2/AboutItem.vue'),
    MeritItem:()=>import('@/components/v2/MeritItem.vue'),
    FlowItem:()=>import('@/components/v2/FlowItem.vue'),
    FeatureItem:()=>import('@/components/v2/FeatureItem.vue'),
    ChargeItem:()=>import('@/components/v2/PriceItem2.vue'),
    FaqItem:()=>import('@/components/v2/FaqItem.vue'),
    Banner:()=>import('@/components/v1/Banner1.vue'),
    FooterItem:()=>import('@/components/FooterItem.vue'),
  },
  data(){
    return {
    }
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()

      setTimeout(() => this.$nuxt.$loading.finish(), 500)
    })
  }
}
</script>

