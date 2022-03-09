<template>
  <button
    @click="onClick"
    class="text-white font-bold pl-6 pr-14 py-6 leading-none text-2xl rounded-lg shadow-lg hover:bg-opacity-70"
    style="background: linear-gradient(to left, #C52475, #FF8B33);"
  >
    <slot>ボタンLサイズ</slot>
    <span class="span1"></span>
    <span class="span2"></span>
  </button>
</template>
<script>
export default {
  name: "ButtonL",
  props: {
    buttonName: {
      type: String,
      default: "null",
    },
  },
  methods: {
    onClick(event) {
      this.$emit('click', event) // このメソッド内で$emitでイベントを定義する第一引数にイベント名、以降の引数に追加の引数を渡す
    }
  }
};
</script>
<style scoped>
button{
  position: relative;
  display: inline-block;
}
button::before {
  position: absolute;
  top: -1px;
  right: -1px;
  bottom: -1px;
  left: -1px;
  z-index: 10;
  content: '';
  background: white;
  opacity: 0.5;
  transform-origin: right top;
  transform: scale(0, 1);
  /* transition: transform .3s; */
  border-radius: 0.5rem;
}
button:hover::before {
  transform-origin: left top;
  transform: scale(1, 1);
}
.span1,
.span2{
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  margin: auto;
  content: "";
  vertical-align: middle;
}
.span1{
  right: 30px;
  width: 18px;
  height: 3px;
  padding: 0;
  border-radius: 1px;
  background: white;
}
.span2{
  right: 30px;
  width: 15px;
  height: 15px;
  border-top: 3px solid white;
  border-right: 3px solid white;
  border-radius: 3px;
  -webkit-transform: rotate(45deg);
  transform: rotate(45deg);
}
</style>