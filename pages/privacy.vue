<template>
  <div id="Privacy">
    <main>
      <HeaderItem/>
      <PrivacyItem/>
      <FooterItem/>
    </main>
  </div>
</template>

<script>
import HeaderItem from '@/components/HeaderItem.vue'
import PrivacyItem from '@/components/PrivacyItem.vue'
import FooterItem from '@/components/FooterItem.vue'


export default {
  name: 'Home',
  components: {
    HeaderItem,
    PrivacyItem,
    FooterItem,
  },
  data(){
    return {
    }
  }
}
</script>

<style>

</style>
