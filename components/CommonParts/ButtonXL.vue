<template>
  <button
    @click="onClick"
    class="text-white font-bold pl-6 pr-14 py-6 leading-none text-2xl rounded-lg shadow-lg"
    style="background: linear-gradient(to left, #C52475, #FF8B33);"
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
  border: 3px solid white;
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
    right: 30px;
    width: 18px;
    height: 3px;
    padding: 0;
    border-radius: 1px;
    background: white;
}
button::after{
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