<template>
  <div>
    <!-- 양방향 데이터 바인딩 v-model -->
    <input type="text" v-model="userId" />
    <!-- @click의 @이 이벤트리스너 -->
    <!-- myFunction에 전달할 파라미터 없으면 () 생략 가능 -->
    <button @click="myFunction">클릭</button>
    <button @click="changeData">변경</button>
    <br>
    <!-- 텍스트로 받아서 문자열 더하기 됨 -->
    <input type="text" v-model="num1"> +
    <input type="text" v-model="num2"> =
    {{num1 + num2}}
    <br>
    <!-- v-model.number로 숫자형 변환 -->
    <input type="text" v-model.number="num3"> +
    <input type="text" v-model.number="num4"> =
    {{num3 + num4}}
  </div>
</template>

<script>
export default {
  data() {
    return {
      userId: 'nanana',
      num1: 0,
      num2: 0,
      num3: 0,
      num4: 0
    }
  },
  methods: {
    // method는 function을 생략
    myFunction() {
      // data를 바인딩 할 때 this 넣어주기
      console.log(this.userId)
    },
    changeData() {
      this.userId = 'changechange'
    }
  }
}
</script>

<style>

</style>
