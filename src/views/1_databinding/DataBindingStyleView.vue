<template>
  <div>
    <div style="color: red; font-size: 30px">스타일 바인딩: red color, 30px font</div>
    <!-- :style=" "에 style1 작성 -->
    <div :style="style1">스타일 바인딩: green color, 30px font</div>
    <!-- method 없이 직접 작성 -->
    <button @click="style1.color='blue'">색상 바꾸기</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // style은 객체 형태로 저장
      style1: {
        color: 'green',
        // camel case로 작성
        fontSize: '30px'
      }
    }
  }
}
</script>

<style>

</style>
