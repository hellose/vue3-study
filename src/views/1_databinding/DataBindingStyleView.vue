<template>
  <div>
    <div style="color: red; font-size: 30px">
      스타일 바인딩: 글씨는 red, 폰트크기:30px
    </div>
    <div :style="styleObject1">스타일 바인딩: 글씨는 red, 폰트크기:30px</div>
    <button @click="styleObject1.color = 'blue'">색상바꾸기</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      styleObject1: {
        color: 'green',
        fontSize: '30px'
      }
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
