<template>
  <div>
    <!-- :class에서 { }로 묶어줌 -->
    <!-- text-red 처럼 -가 들어가면 ' '로 묶어주기 -->
    <!-- 일반 단어면 ' ' 생략 가능 -->
    <div :class="{'text-red': hasError, active: isActive}">클래스 바인딩</div>
    <!-- :class에 중괄호 없이 class2 넣으면 배열에 있는 모든 class 적용 -->
    <div :class="class2">또 다른 클래스 바인딩</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // class에 적용할 bool 변수
      isActive: false,
      hasError: true,
      // 두 개 이상의 클래스 넣을 때 배열
      class2: ['active', 'text-red']
    }
  }
}
</script>
<!-- scope 넣어줘야 현재 파일에서만 스타일 적용 -->
<style scope>
.active {
  background-color: greenyellow;
  font-weight: bold;
}

.text-red {
  color: red;
}
</style>
