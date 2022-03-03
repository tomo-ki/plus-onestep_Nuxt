<template>
  <section id="header" class="flex items-center justify-between px-16 fixed bg-white bg-opacity-70 w-full z-20 h-16 ">
    <div class="">
      <router-link to="#top">
        <img src="../assets/img/index/onestep/onestep_line.svg" alt="+one step">
      </router-link>
    </div>
    <div>
      <ul class="flex">
        <li><router-link to="#top">+one stepとは</router-link></li>
        <li class="ml-10"><router-link to="#top">+one stepとは</router-link></li>
        <li class="ml-10"><router-link to="#top">+one stepとは</router-link></li>
        <li class="ml-10"><router-link to="#top">+one stepとは</router-link></li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Header',
  components: {
  },
  data(){
    return {
    }
  }
}
</script>

<style>

</style>
