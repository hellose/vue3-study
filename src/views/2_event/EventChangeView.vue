<template>
  <div>
    <select name="" id="" @change="changeCity($event)" v-model="selectedCity">
      <option value="" default>지역선택</option>
      <option
        v-for="city in cityList"
        :key="city.cityCode"
        :value="city.cityCode"
      >
        {{ city.title }}
      </option>
    </select>
    <select name="" id="">
      <option
        v-for="dong in selectedDongList"
        :key="dong.dongCode"
        :value="dong.dongCode"
      >
        {{ dong.dongTitle }}
      </option>
    </select>
    <select name="" id="">
      <option
        v-for="dong in dongList.filter((obj) => selectedCity === obj.cityCode)"
        :key="dong.dongCode"
        :value="dong.dongCode"
      >
        {{ dong.dongTitle }}
      </option>
    </select>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      cityList: [
        { cityCode: '02', title: '서울' },
        { cityCode: '051', title: '부산' },
        { cityCode: '064', title: '제주' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: '서울 1동' },
        { cityCode: '02', dongCode: '2', dongTitle: '서울 2동' },
        { cityCode: '02', dongCode: '3', dongTitle: '서울 3동' },
        { cityCode: '051', dongCode: '1', dongTitle: '부산 1동' },
        { cityCode: '051', dongCode: '2', dongTitle: '부산 2동' },
        { cityCode: '051', dongCode: '3', dongTitle: '부산 3동' },
        { cityCode: '064', dongCode: '1', dongTitle: '제주 1동' },
        { cityCode: '064', dongCode: '2', dongTitle: '제주 2동' },
        { cityCode: '064', dongCode: '3', dongTitle: '제주 3동' }
      ],
      selectedCity: '',
      selectedDongList: []
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    changeCity(event) {
      console.log(event)
      this.selectedDongList = this.dongList.filter(
        (obj) => obj.cityCode === this.selectedCity
      )
    }
  }
}
</script>
