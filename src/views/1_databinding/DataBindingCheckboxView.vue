<template>
  <div>
    <div>
      <!-- input id와 label for 맞추기 -->
      <!-- checked된 value로 양방향 데이터 바인딩 -->
      <input
        type="checkbox"
        id="html"
        value="HTML"
        v-model="favoriteLang">
      <label for="html">HTML</label>
    </div>
    <div>
      <input
        type="checkbox"
        id="css"
        value="CSS"
        v-model="favoriteLang">
      <label for="css">CSS</label>
    </div>
    <div>
      <input
        type="checkbox"
        id="js"
        value="JS"
        v-model="favoriteLang">
      <label for="js">JavaScript</label>
    </div>
    <div>선택한 언어: {{favoriteLang}}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // checkbox의 value와 같은 값 있으면 체크 된 상태로 시작
      favoriteLang: ['JS']
    }
  }
}
</script>

<style>

</style>
