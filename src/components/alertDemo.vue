<template>
  <div>
    <group>
      <switch title="Toggle" :value.sync="show"></switch>
    </group>
    <alert :show.sync="show" title="恭喜你" button-text="恭喜你,调用了一个alert"
           @on-show="onShow" @on-hide="onHide">
      <p style="text-align:center;">中大奖了！99999元只要转4000元手续费</p>
    </alert>
  </div>
</template>
<style>
  body {
  }
</style>
<script>
  import Group from '../vux/components/group/index.vue'
  import Switch from '../vux/components/switch/index.vue'
  import Alert from '../vux/components/alert/index.vue'
  export default{
    data () {
      return {
        show: false
      }
    },
    components: {
      Group, Switch, Alert
    },
    methods: {
      onShow: function () {
        console.log('onShow 啦')
      },
      onHide: function () {
        console.log('onHide 啦')
      }
    }
  }
</script>
