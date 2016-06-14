<template>
  <div id="app">
    <!--<flex></flex>-->
    <!--<scrollbar></scrollbar>-->
    <!--<tab></tab>-->
    <!--<popup></popup>-->
    <!--<button-tab></button-tab>-->
    <!--<sticky></sticky>-->
    <!--<tab-bar></tab-bar>-->
    <!--<timeline-demo></timeline-demo>-->
    <!--<x-header-demo></x-header-demo>-->
    <!--<brade-demo></brade-demo>-->
    <!--<icon-demo></icon-demo>-->
    <group-demo></group-demo>
  </div>
</template>

<script>
  //  import Flex from './components/FlexDemo.vue'
  //  import Scrollbar from './components/Scrollbar.vue'
  //  import Tab from './components/Tab.vue'
  //  import Popup from './components/Popup.vue'
  //  import ButtonTab from './components/buttomTab.vue'
  //  import Sticky from './components/sticky.vue'
  //  import TabBar from './components/tabBar.vue'
  //  import TimelineDemo from './components/timeLineDemo.vue'
  //  import XHeaderDemo from './components/xHeaderDemo.vue'
  //  import BradeDemo from './components/bradeDemo.vue'
//  import IconDemo from './components/iconDemo.vue'
  import GroupDemo from './components/groupDemo.vue'

  export default {
    components: {
//      Flex,
//      Scrollbar,
//      Tab,
//      Popup
//      ButtonTab
//      Sticky
//      TabBar
//      TimelineDemo
//      XHeaderDemo
//      BradeDemo
//      IconDemo
      GroupDemo
    }
  }
</script>

<style lang="less">
  @import './vux/styles/index.less';
  body {
    font-family: Helvetica, sans-serif;
    background-color: #fbf9fe;
    padding-bottom:50px;
  }
</style>

