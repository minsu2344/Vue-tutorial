<template>
  <div>
    <div>
      <select name="" id="">
        <!-- v-for="city in cities"를 이용하면 cities 길이만큼 option 생성 -->
        <!-- :key 필수로 넣어줘야 함 -->
        <!-- city 변수 사용 가능 -->
        <option :value="city.code" v-for="city in cities" :key="city.code">{{city.title}}</option>
      </select>
    </div>
    <!-- 음료 테이블 만들기 -->
    <div>
      <table>
        <thead>
          <tr>
            <th>제품번호</th>
            <th>제품명</th>
            <th>가격</th>
            <th>수량</th>
            <th>합계</th>
          </tr>
        </thead>
        <tbody>
          <!-- 두 번째 매개변수인 index를 받아 :key에 넣어줘도 됨 -->
          <tr v-for="(drink, idx) in drinkList" :key="idx">
            <td>{{drink.drinkId}}</td>
            <td>{{drink.drinkName}}</td>
            <td>{{drink.price}}</td>
            <!-- 수량은 v-model로 변경 가능 -->
            <td><input type="number" v-model="drink.quantity"></td>
            <td>{{drink.price * drink.quantity}}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cities: [
        { title: '서울', code: '02' },
        { title: '대전', code: '042' },
        { title: '제주', code: '064' }
      ],
      drinkList: [
        {
          drinkId: '1',
          drinkName: '코카콜라',
          price: 700,
          quantity: 1
        },
        {
          drinkId: '2',
          drinkName: '제로 사이다',
          price: 900,
          quantity: 1
        },
        {
          drinkId: '3',
          drinkName: '델몬트 오렌지',
          price: 1200,
          quantity: 3
        },
        {
          drinkId: '4',
          drinkName: '토마토 주스',
          price: 600,
          quantity: 1
        },
        {
          drinkId: '5',
          drinkName: '꿀맛 ZICO',
          price: 100,
          quantity: 6
        }
      ]
    }
  }
}
</script>

<style>

</style>
