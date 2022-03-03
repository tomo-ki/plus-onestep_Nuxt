<template>
  <button
    @click="onClick"
    class="text-white border pl-9 pr-4 py-3 leading-none text-sm rounded-lg shadow-lg hover:opacity-70"
    style="background: linear-gradient(to left, #078C7A, #0D81B0);">
    <slot>ボタンミニ</slot>
  </button>
</template>
<script>
export default {
  name: "ButtonSL",
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
button::before,
button::after{
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  margin: auto;
  content: "";
  vertical-align: middle;
}
button::before{
  left: 14px;
  width: 14px;
  height: 2px;
  padding: 0;
  border-radius: 1px;
  background: white;
}
button::after{
  left: 14px;
  width: 10px;
  height: 10px;
  border-top: 2px solid white;
  border-left: 2px solid white;
  border-radius: 2px;
  -webkit-transform: rotate(-45deg);
  transform: rotate(-45deg);
}
</style>