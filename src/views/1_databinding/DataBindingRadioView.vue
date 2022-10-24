<template>
  <div>
    <div>
      <!-- checkbox와 type만 다름 -->
      <input type="radio" name="" id="html" value="HTML" v-model="favoriteLang">
      <label for="html">HTML</label>
    </div>
    <div>
      <input type="radio" name="" id="css" value="CSS" v-model="favoriteLang">
      <label for="css">CSS</label>
    </div>
    <div>
      <input type="radio" name="" id="js" value="JS" v-model="favoriteLang">
      <label for="js">JavaScript</label>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // radio는 하나만 선택 가능하므로 string으로 변경
      favoriteLang: ''
    }
  }
}
</script>

<style>

</style>
