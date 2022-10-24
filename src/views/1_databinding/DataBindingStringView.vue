<template>
  <div>
    <h1>Hello {{userName}}</h1>
    <p>{{message}}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      userName: 'minsoo',
      message: 'welcome!!',
      arr: [],
      obj: {}
    }
  }
}
</script>
<style scoped>

</style>
