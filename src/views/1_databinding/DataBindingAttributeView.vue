<template>
  <div>
    <!-- v-bind-value로 value값 단방향 데이터 바인딩 -->
    <input type="text" v-bind:value="userId" readonly>
    <!-- v-bind 생략 가능 -->
    <input type="text" :value="userId" readonly>
    <br>
    <!-- src에 바인딩 -->
    <img :src="imgSrc" alt="" style="width: 100px; height: auto;">
    <br>
    <!-- input에 값이 없으면 button 비활성화 하기 -->
    <input type="search" v-model="txt1">
    <button :disabled="txt1 === ''">조회</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userId: 'abc',
      imgSrc: '/favicon.ico',
      txt1: ''
    }
  }
}
</script>

<style>

</style>
