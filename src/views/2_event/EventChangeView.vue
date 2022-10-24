<template>
  <div>
    <!-- change 이벤트 및 v-model 작성 -->
    <!-- @change와 v-on:change 모두 가능 -->
    <!-- 매개변수로 event를 전달할 때는 $ 사용 -->
    <select
      v-on:change="changeCity($event)"
      v-model="selectedCity"
    >
      <option value="">==도시선택==</option>
      <option
        :value="city.cityCode"
        :key="city.cityCode"
        v-for="city in cityList"
      >
        {{city.title}}
      </option>
    </select>
    <!-- 첫 select 선택에 따라 달라지는 이중 select -->
    <select>
      <option
        :value="dong.dongCode"
        :key="dong.dongCode"
        v-for="dong in selectedDongList"
      >
        {{dong.dongTitle}}
      </option>
    </select>
    <!-- option에 직접 필터링 -->
    <!-- v-for에는 this 안 씀 -->
    <select>
      <option
        :value="dong.dongCode"
        :key="dong.dongCode"
        v-for="dong in dongList.filter(dong => dong.cityCode === selectedCity)"
      >
        {{dong.dongTitle}}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // 첫 select에서 선택한 도시 코드
      selectedCity: '',
      cityList: [
        { cityCode: '02', title: '서울' },
        { cityCode: '042', title: '대전' },
        { cityCode: '064', title: '제주' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: '서울 1동' },
        { cityCode: '02', dongCode: '2', dongTitle: '서울 2동' },
        { cityCode: '02', dongCode: '3', dongTitle: '서울 3동' },
        { cityCode: '02', dongCode: '4', dongTitle: '서울 4동' },
        { cityCode: '042', dongCode: '1', dongTitle: '대전 1동' },
        { cityCode: '042', dongCode: '2', dongTitle: '대전 2동' },
        { cityCode: '064', dongCode: '1', dongTitle: '제주 1동' },
        { cityCode: '064', dongCode: '2', dongTitle: '제주 2동' }
      ],
      // 두 번째 select option에 들어갈 동
      selectedDongList: []
    }
  },
  methods: {
    // 도시가 바뀔 때마다 바뀌는 selectedDongList
    // event 받을 때 매개변수 맘대로 지정 가능
    changeCity(evt) {
      console.log(evt.target.tagName)
      this.selectedDongList = this.dongList.filter(dong => dong.cityCode === this.selectedCity)
    }
  }
}
</script>

<style>

</style>
