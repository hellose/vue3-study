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
