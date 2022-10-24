<template>
  <div>
    <!-- @keyup에 event 보내서 enter 키 확인 -->
    <input type="search" @keyup="checkEnter($event)" v-model="searchText">
    <button @click="doSearch">조회</button>
    <!-- @keyup.enter로 엔터 바로 확인 -->
    <!-- .enter, .tab, .delete, .esc, .space, .up, .down, .left, .right, .ctrl.enter(컨트롤+엔터) 등 다양함 -->
    <input type="search" @keyup.enter="doSearch" v-model="searchText">
    <button @click="doSearch">조회</button>
    <!-- .stop - event.stopPropagation -->
    <!-- .prevent - event.preventDefault() -->
    <button type="submit" @click.prevent="doSearch">제출</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchText: ''
    }
  },
  methods: {
    doSearch() {
      console.log(this.searchText)
    },
    checkEnter(evt) {
      console.log(evt.key)
      // key가 enter면 doSearch 실행
      if (evt.key === 'Enter') {
        // method도 this 사용
        this.doSearch()
      }
    }
  }
}
</script>

<style>

</style>
