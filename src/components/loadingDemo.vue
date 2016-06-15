<template>
  <div>
    <group>
      <switch title="Toggle" :value.sync="show" @on-change="delayHide"></switch>
    </group>
    <loading :show="show" :text="text1"></loading>
  </div>
</template>
<style>
  body {
  }
</style>
<script>
  import Group from '../vux/components/group/index.vue'
  import Switch from '../vux/components/switch/index.vue'
  import Loading from '../vux/components/loading/index.vue'
  export default{
    data () {
      return {
        show: false,
        text1: '这是loading'
      }
    },
    components: {
      Group, Switch, Loading
    },
    methods: {
      delayHide: function () {
        var _this = this
        setTimeout(function () {
          _this.show = false
        }, 1500)
      }
    }
  }
</script>
