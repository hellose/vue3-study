<template>
  <div>
    <button @click="increaseCounter">increase 1</button>
    <p>{{ count }}</p>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      count: 0
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    increaseCounter() {
      this.count = this.count + 1
    }
  }
}
</script>
