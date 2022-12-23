<template>
  <div>
    <input type="text" v-model="userId" /><br />
    <span>data-userId값: {{ userId }} </span>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'sehyun'
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
