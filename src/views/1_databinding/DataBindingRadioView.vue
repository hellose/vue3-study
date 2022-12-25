<template>
  <div>
    <div>
      <input type="radio" id="html" value="HTML" v-model="favoriteLanguage" />
      <label for="html">HTML</label>
    </div>
    <div>
      <input type="radio" id="css" value="CSS" v-model="favoriteLanguage" />
      <label for="css">CSS</label>
    </div>
    <div>
      <input type="radio" id="js" value="JS" v-model="favoriteLanguage" />
      <label for="js">JS</label>
    </div>
    <div>선택한 언어: {{ favoriteLanguage }}</div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      favoriteLanguage: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
