<template>
  <div>
    <h1>v-model</h1>
    <input type="text" v-model="userId" />
    <br />
    <h1>v-model 은 string으로</h1>
    <input type="text" v-model="num1" /> +
    <input type="text" v-model="num2" /> =
    <span>{{ num1 + num2 }} </span>
    <br />
    <h1>v-model.number 를 사용</h1>
    <input type="text" v-model.number="num3" /> +
    <input type="text" v-model.number="num4" /> =
    <span>{{ num3 + num4 }} </span>
    <br />
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'sehyun',
      num1: 0,
      num2: 0,
      num3: 0,
      num4: 0
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    myFunction() {
      console.log(this.userId)
    }
  }
}
</script>
