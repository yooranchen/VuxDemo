<template>
  <div>
    <group>
      <switch title="Toggle" :value.sync="show"></switch>
    </group>
    <confirm :show.sync="show" title="是否要退出呢" cancel-text="取消" confirm-text="退出"
             @on-confirm="onAction('确认')" @on-cancel="onAction('取消')"
    >
      <p style="text-align:center;">中大奖了！99999元只要转4000元手续费</p>
    </confirm>
    <toast :show.sync="showToast" type="warn" :time="cancel">{{toastText}}</toast>
  </div>
</template>
<style>
  body {
  }
</style>
<script>
  import Group from '../vux/components/group/index.vue'
  import Switch from '../vux/components/switch/index.vue'
  import Confirm from '../vux/components/confirm/index.vue'
  import Toast from '../vux/components/toast/index.vue'
  export default{
    data () {
      return {
        show: false,
        showToast: false,
        toastText: '',
        time: 1000,
        type: 'warn'
      }
    },
    components: {
      Group, Switch, Confirm, Toast
    },
    methods: {
      onAction: function (type) {
        if (type === '确认') {
          this.time = 3000
        } else {
          this.time = 1000
        }
        this.showToast = true
        this.toastText = type + this.time
      }
    }
  }
</script>
