<template>
  <div>
    <group title="I'm a group title">
      <cell title="cell" value="Hello world" inline-desc="我是第二行文字" is-link></cell>
      <x-input title="输入内容" :value.sync="value" v-ref:input is-type="china-mobile"></x-input>
      <cell title="验证xInput输入内容" :value="'$valid value: '+ $refs.input.valid"></cell>
      <switch title="switch"></switch>
      <x-textarea placeholder="这是输入框"></x-textarea>
      <calendar title="Calendar"></calendar>
      <x-button type="primary" @click="btnChangeText" :disabled="isDisabled">{{btnText}}</x-button>
    </group>
    <group title="I'm another group title" title-color="green">
      <cell title="cell" value="hello world" is-link></cell>
      <x-input title="x-input"></x-input>
      <x-number title="x-number" @on-change="change"></x-number>
    </group>
  </div>
</template>
<style>
</style>
<script>
  import Group from '../vux/components/group/index.vue'
  import Cell from '../vux/components/cell/index.vue'
  import XInput from '../vux/components/x-input/index.vue'
  import Switch from '../vux/components/switch/index.vue'
  import XTextarea from '../vux/components/x-textarea/index.vue'
  import XNumber from '../vux/components/x-number/index.vue'
  import XButton from '../vux/components/x-button/index.vue'
  import Calendar from '../vux/components/calendar/index.vue'
  export default{
    data () {
      return {
        btnText: '点击进行提交',
        isDisabled: false,
        value: ''
      }
    },
    components: {
      Group,
      Cell,
      XInput,
      Switch,
      XTextarea,
      XNumber,
      Calendar,
      XButton
    },
    methods: {
      btnChangeText: function () {
        const _this = this
        this.isDisabled = true
        this.btnText = '正在提交中'
        setTimeout(function () {
          _this.btnText = '提交完成'
          _this.isDisabled = false
        }, 5000)
      },
      change: function (number) {
        console.log(number)
      }
    }
  }
</script>
