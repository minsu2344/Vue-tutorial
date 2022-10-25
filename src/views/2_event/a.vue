<template>
  <div>
    <div class="newModal" v-if="modalStatus">
      <h3>모달</h3>
      <p>모달 페이지 입니다.</p>
    </div>
    <div>
      <button @click="modalStatus = true">모달 열기</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      modalStatus: false
    }
  }
}
</script>
