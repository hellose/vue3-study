<template>
  <div>
    <div :class="{ active: isActive, 'text-red': hasError }">클래스 바인딩</div>
    <br />
    <div :class="list">클래스 바인딩2</div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      isActive: true,
      hasError: true,
      list: ['active', 'text-red']
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>

<style scoped>
.active {
  background-color: greenyellow;
  font-weight: bold;
}

.text-red {
  color: red;
}
</style>
