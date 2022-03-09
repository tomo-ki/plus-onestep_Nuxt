<template>
  <section id="header" >
    <div class="hidden sm:flex items-center justify-between px-16 fixed bg-white bg-opacity-70 w-full z-20 h-16">
      <div class="">
        <!-- <router-link to="#top">
          <img src="../assets/img/index/onestep/onestep_line.svg" alt="+one step">
        </router-link> -->
        <button @click="scrollTop()" class="cursor-pointer">
          <img src="../assets/img/index/onestep/onestep_line.svg" alt="+one step">
        </button>
      </div>
      <div class="">
        <ul class="flex">
          <li><button @click="onClick" v-scroll-to="'#about'">+one stepとは</button></li>
          <li class="ml-10"><button @click="onClick" v-scroll-to="'#merit'">導入メリット</button></li>
          <li class="ml-10"><button @click="onClick" v-scroll-to="'#flow'">活用方法</button></li>
          <li class="ml-10"><button @click="onClick" v-scroll-to="'#price'">料金プラン</button></li>
          <li class="ml-10"><button @click="onClick" v-scroll-to="'#faq'">よくあるご質問</button></li>
        </ul>
      </div>
    </div>
    <div class="sm:hidden fixed w-full z-30">
      <div  v-if="valMenu == false" class="flex justify-center items-center h-16 bg-white bg-opacity-70">
        <div class="w-full sp-head">
          <button @click="scrollTop()" class="inline-block w-full flex items-center justify-center">
            <img class="h-10" src="../assets/img/index/onestep/onestep_line.svg" alt="+one step">
          </button>
          <div @click="menuToggle()" class="hbg-wrap">
            <div class="hbg">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </div>
        </div>
      </div>
      <div  v-if="valMenu == true" class="flex justify-center items-center h-16 bg-white">
        <div class="w-full sp-head">
          <button @click="scrollTop()" class="inline-block w-full flex items-center justify-center">
            <img class="h-10" src="../assets/img/index/onestep/onestep_line.svg" alt="+one step">
          </button>
          <div @click="menuToggle()" class="hbg-wrap">
            <div class="hbg-cross">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </div>
        </div>
      </div>
      <div class="bg-white h-screen w-full" v-if="valMenu == true">
        <ul class="flex flex-col text-xl w-full">
          <li class="sm-li w-full h-20 text-center flex items-center" style="line-height:80px;">
            <button @click="onClick()" v-scroll-to="'#about'" class="w-full h-full inline-block">
              +one stepとは
            </button>
          </li>
          <li class="sm-li w-full h-20 text-center flex items-center" style="line-height:80px;">
            <button @click="onClick()" v-scroll-to="'#merit'" class="w-full h-full inline-block">
              導入メリット
            </button>
          </li>
          <li class="sm-li w-full h-20 text-center flex items-center" style="line-height:80px;">
            <button @click="onClick()" v-scroll-to="'#flow'" class="w-full h-full inline-block">
              活用方法
            </button>
          </li>
          <li class="sm-li w-full h-20 text-center flex items-center" style="line-height:80px;">
            <button @click="onClick()" v-scroll-to="'#price'" class="w-full h-full inline-block">
              料金プラン
            </button>
          </li>
          <li class="sm-li w-full h-20 text-center flex items-center" style="line-height:80px;">
            <button @click="onClick()" v-scroll-to="'#faq'" class="w-full h-full inline-block">
              よくあるご質問
            </button>
          </li>
        </ul>
      </div>
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
      valMenu: false,
    }
  },
  methods: {
    menuToggle(){
      if(this.valMenu == false){
        this.valMenu = true;
      }
      else{
        this.valMenu = false;
      }
    },
    scrollTop(){
      if(window.innerWidth <= 640){
        if(this.valMenu == true){
          this.menuToggle()
        }
      }
      scrollTo({
        top: 0,
        behavior: "smooth"
      })
    },
    onClick(event) {
      this.$emit('click', event)
    },
  }
}
</script>

<style>
.sm-li:hover{
  background-color:#B9E6D3;
}
.sp-head{
  position: relative;
}
.hbg-wrap{
  position: absolute;
  top: -5px;
  right: 10px;
}
.hbg,.hbg-cross{
  position: relative;
	cursor: pointer;
  width: 50px;
  height:50px;
	border-radius: 5px;
}
.hbg span,.hbg-cross span{
  display: inline-block;
  transition: all .4s;/*アニメーションの設定*/
  position: absolute;
  left: 14px;
  height: 3px;
  border-radius: 2px;
	background: #9E9E9E;
  width: 45%;
}
.hbg span:nth-of-type(1) {
	top:15px;
}

.hbg span:nth-of-type(2) {
	top:23px;
}

.hbg span:nth-of-type(3) {
	top:31px;
}

.hbg-cross span:nth-of-type(1) {
    top: 18px;
    left: 12px;
    transform: translateY(6px) rotate(-45deg);
    width: 50%;
}

.hbg-cross span:nth-of-type(2) {
	opacity: 0;/*真ん中の線は透過*/
}

.hbg-cross span:nth-of-type(3){
    top: 30px;
    left: 12px;
    transform: translateY(-6px) rotate(45deg);
    width: 50%;
}
</style>
