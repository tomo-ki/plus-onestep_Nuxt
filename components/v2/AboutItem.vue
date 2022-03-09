<template>
  <section id="about" class="flex flex-col items-center w-full py-16">
    <h2 class="flex items-center mb-16 sm:hidden">
      <img src="../../assets/img/index/onestep/onestep_line.svg" alt="+one step">
      <span class="text-2xl sm:text-3xl font-bold ml-4">
        とは
      </span>
    </h2>
    <div class="w-full">
      <div class="flex flex-col sm:flex-row-reverse mb-20">
        <div class="sm:w-7/12">
          <img src="../../assets/img/index/about/about_v2_img1.svg" alt="" class="w-full">
        </div>
        <div
          class="py-20 sm:py-0 sm:pl-24 flex flex-col items-center sm:items-start sm:w-5/12"
        >
          <h2 class="sm:flex items-center mb-10 hidden z-10">
            <img src="../../assets/img/index/onestep/onestep_line.svg" alt="+one step">
            <span class="text-2xl sm:text-2xl font-bold ml-4">
              とは
            </span>
          </h2>
          <div class="w-9/10 relative">
            <img
              src="../../assets/img/index/about/about_v2_01.png"
              alt="01" class="absolute left-0 sm:left-full sm:transform sm:-translate-x-3/4 -top-12 sm:-top-20 z-0 w-3/12 sm:w-4/12"
            >
            <p class="text-lg leading-8 absolute z-10">
              + one stepとは、コミュニティ形成、新規採用、従業員定着支援が一元管理出来る、公式LINE拡張ツールです。
            </p>
          </div>
        </div>
      </div>
      <div class="flex flex-col sm:flex-row sm:pr-20">
        <div class="flex justify-start sm:w-7/12">
          <img src="../../assets/img/index/about/about_v2_img2.svg" alt="about2" class="w-full inline-block">
        </div>
        <div
          class="py-20 flex flex-col items-center sm:w-5/12"
        >
          <div class="w-9/10 relative">
            <img
              src="../../assets/img/index/about/about_v2_02.png"
              alt="02" class="absolute right-0 -top-12 z-0 sm:-top-20 w-3/12 sm:w-4/12"
            >
            <p class="text-lg leading-8 absolute z-10">
                新規採用したい、顧客／従業員とのコミュニケーションを活発にしたい、従業員の離職を防ぎたいといったお悩みを一手に解決いたします！
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Number01 from "@/assets/img/index/about/about_v2_01.svg"
import Number02 from "@/assets/img/index/about/about_v2_02.svg"

export default {
  name: 'About',
  components: {
  },
  data(){
    return {
      number01: Number01,
      number02: Number02,
    }
  }
}
</script>
