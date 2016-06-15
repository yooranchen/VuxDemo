<template>
  <div>
    <group title="dialog demo">
      <switch title="打开dialog" :value.sync="show1" @on-change="onChange"></switch>
    </group>
    <dialog :show.sync="show1" class="dialog-demo" @on-show="onShow" @on-hide="onHide" 	dialog-transition>
      <p class="dialog-title">I'm a Dialog.</p>
    </dialog>
  </div>
</template>
<style>
  body {
  }
</style>
<script>
  import Group from '../vux/components/group/index.vue'
  import Switch from '../vux/components/switch/index.vue'
  import Dialog from '../vux/components/dialog/index.vue'
  export default{
    data () {
      return {
        show1: false
      }
    },
    components: {
      Group, Switch, Dialog
    },
    methods: {
      onShow: function () {
        console.log('对话框显示')
      },
      onHide: function () {
        console.log('对话框隐藏')
      },
      onChange: function () {
       console.log(this.show1)
      }
    }
  }
</script>
