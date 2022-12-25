<template>
  <div>
    <select v-model="selectedCity">
      <option value="" selected></option>
      <option value="02">서울</option>
      <option value="051">부산</option>
      <option value="064">제주</option>
    </select>
    <br /><br />
    <span>selectedCity: {{ selectedCity }}</span>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      selectedCity: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
