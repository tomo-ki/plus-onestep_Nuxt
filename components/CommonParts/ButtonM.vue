<template>
  <button
    @click="onClick"
    class="text-white border pl-8 pr-12 py-5 leading-none text-xl rounded-lg shadow-lg"
    style="background: linear-gradient(to left, #078C7A, #0D81B0);">
    <slot>ボタンMサイズ</slot>
    <span class="span1"></span>
    <span class="span2"></span>
  </button>
</template>
<script>
export default {
  name: "ButtonM",
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
  transition: transform .3s;
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
  right: 20px;
  width: 18px;
  height: 2px;
  padding: 0;
  border-radius: 1px;
  background: white;
}
.span2{
    right: 20px;
    width: 15px;
    height: 15px;
    border-top: 2px solid white;
    border-right: 2px solid white;
    border-radius: 2px;
    -webkit-transform: rotate(45deg);
    transform: rotate(45deg);
}
</style>