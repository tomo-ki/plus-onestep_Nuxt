<template>
  <button
    @click="onClick"
    class="border pl-8 pr-12 py-5 leading-none text-xl rounded-lg shadow-lg"
    style="color:#3AAEA7; border:2px solid #3AAEA7;">
    <slot>ボタンMサイズ</slot>
  </button>
</template>
<script>
export default {
  name: "ButtonMminus",
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
    right: 20px;
    width: 15px;
    height: 2px;
    padding: 0;
    border-radius: 1px;
    background: #3AAEA7;
}
</style>