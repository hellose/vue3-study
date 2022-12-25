<template>
  <div>
    <p>One way binding</p>
    <input type="text" v-bind:value="userId" />
    <br />
    <p>Two way binding</p>
    <input type="text" v-model="userId" />
    <br />
    <br />
    <span>userId: {{ userId }}</span>
    <br />
    <img :src="imgSrc" alt="no imsage" style="width: 400px; height: auto" />
    <br />
    <input type="search" v-model="txt1" />
    <button :disabled="txt1 === ''">조회</button>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      userId: 'sehyun',
      imgSrc: 'https://upload.wikimedia.org/wikipedia/commons/f/f1/Vue.png',
      txt1: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
