<template>
  <div>
    <group title="ActionSheet">
      <switch title="ActionSheet 只有选项" :value.sync="show1"></switch>
      <switch title="ActionSheet 带取消按钮" :value.sync="show2"></switch>
      <switch title="ActionSheet 点击事件处理" :value.sync="show3"></switch>
    </group>
    <actionsheet :show.sync="show1" :menus="menus1"></actionsheet>
    <actionsheet :show.sync="show2" :menus="menus2" show-cancel></actionsheet>
    <actionsheet :show.sync="show3" :menus="menus3" show-cancel cancel-text="来取消我啊"
                 @menu-click="itemClick"></actionsheet>
  </div>
</template>
<style>
  body {
  }
</style>
<script>
  import Actionsheet from '../vux/components/actionsheet/index.vue'
  import Group from '../vux/components/group/index.vue'
  import Switch from '../vux/components/switch/index.vue'
  export default{
    data () {
      return {
        show1: false,
        menus1: {
          menu1: 'Share to friends',
          menu2: 'Share to timeline'
        },
        show2: false,
        menus2: {
          menu1: 'Take Photo',
          menu2: 'Choose from photos'
        },
        show3: false,
        menus3: {
          menu1: 'friends comment',
          menu2: 'friends comment2'
        }
      }
    },
    components: {
      Actionsheet, Group, Switch
    },
    methods: {
      itemClick: function (menuKey, menuValue) {
        if (menuKey === 'menu1') {
          console.log('点了第一个')
        } else {
          console.log('点了第二个');
        }
//        console.log(menuKey)
//        console.log(menuValue)
      }
    }
  }
</script>
