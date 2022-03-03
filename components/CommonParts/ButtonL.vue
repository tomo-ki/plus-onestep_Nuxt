<template>
  <button
    @click="onClick"
    class="text-white pl-8 pr-16 py-6 leading-none text-2xl rounded-lg shadow-lg"
    style="background: linear-gradient(to left, #078C7A, #0D81B0);"
  >
    <slot>ボタンLサイズ</slot>
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
button::before,
button::after{
    position: absolute;
    top: 0;
    bottom: 0;
    right: 0;
    margin: auto;
    content: "";
    vertical-align: middle;
}
button::before{
    right: 40px;
    width: 18px;
    height: 2px;
    padding: 0;
    border-radius: 1px;
    background: white;
}
button::after{
    right: 40px;
    width: 15px;
    height: 15px;
    border-top: 2px solid white;
    border-right: 2px solid white;
    border-radius: 2px;
    -webkit-transform: rotate(45deg);
    transform: rotate(45deg);
}
</style>