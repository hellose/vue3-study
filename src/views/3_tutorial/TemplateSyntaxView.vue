<template>
  <div>
    <h1>Template Syntax</h1>
    <hr />
    <h3>1. Text Interpolation</h3>
    <h4>설명: data 프로퍼티에 해당하는 값 셋팅</h4>
    <span>Message: {{ msg }}</span>
    <br />
    <hr />

    <h3>2. v-html directive</h3>
    <h4>설명: innerHTML 셋팅</h4>
    <p>Using text interpolation: {{ rawHtml }}</p>
    <p>Using v-html directive: <span v-html="rawHtml"></span></p>
    <hr />

    <h3>3. v-bind directive is used to reactively update an HTML attribute</h3>
    <h4>설명: 바인딩 값이 null 또는 undefined인경우 속성은 제거됨</h4>
    <p v-bind:id="pElementId">p 엘리먼트 id attribute바인딩</p>
    <p :id="pElementId2">v-bind:id는 :id와 동일 (v-bind생략가능)</p>
    <hr />

    <h3>4. v-bind with HTML boolean Attributes</h3>
    <h4>설명: truthy, falsy 확인된 후 boolean Attribute 반영</h4>
    <button :disabled="true">true</button><br />
    <button :disabled="false">false</button><br />
    <button :disabled="propertyNull">null</button><br />
    <button :disabled="propertyUndefined">undefined</button><br />
    <button :disabled="propertyTruthy">truthy value(1)</button><br />
    <button :disabled="propertyFalsy">falsy value(0)</button><br />
    <hr />

    <h3>5. Dynamically Binding Multiple Attributes</h3>
    <p v-bind="objectOfAttrs">여러 attribute를 한번에 바인딩</p>
    <hr />

    <h3>6. Directive | Argument | Dynamic Argument | Modifier</h3>
    <img
      style="width: 50%; height: 50%"
      src="https://vuejs.org/assets/directive.69c37117.png"
      alt="No Image"
    />
    <h4>
      설명: v-on:click.ctrl<br />Directive: v-on <br />Argument: click
      <br />Modifier: ctrl<br />설명:v-on:[attributeName] <br />Dynamic
      Argument: attributeName data property <br />
      attributeName가 동적으로 Argument에 반영
    </h4>
    <hr />

    <h3>7. Dynamic Argument Test</h3>
    <h4>
      Dynamic Argument Value Constraints: Dynamic argument는 string으로 평가됨.
      null사용시 바인딩 제거 <br />Dynamic Argument Syntax Constraints: [
      ]사이에 ', 공백 사용불가
    </h4>
    <span>이벤트이름 입력 </span><input type="text" v-model="eventName" />
    <button v-on:[eventName]="doSomething">v-on:{{ eventName }}</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      msg: 'hello guys',
      rawHtml: '<span style="color: red">This should be red.</span>',
      pElementId: 'pId',
      pElementId2: 'pId2',
      propertyNull: null,
      propertyUndefined: undefined,
      propertyTruthy: 1,
      propertyFalsy: 0,
      objectOfAttrs: {
        id: 'container',
        class: 'test-class'
      },
      eventName: 'click'
    }
  },
  methods: {
    doSomething() {
      console.log(this.eventName)
    }
  }
}
</script>
