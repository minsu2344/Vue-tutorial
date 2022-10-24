<template>
  <div>
    <!-- v-model로 양방향 데이터 바인딩 가능 -->
    <!-- 값 바뀔 때마다 selectedCity도 변경됨 -->
    <select name="" id="" v-model="selectedCity">
      <option value="02">서울</option>
      <option value="042">대전</option>
      <option value="064">제주</option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedCity: '02'
    }
  }
}
</script>

<style>

</style>
