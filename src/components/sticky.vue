<template>
  <div>
    <br v-for="i in 8">
    <sticky>
      <tab :line-width=1>
        <tab-item :selected="demo === item" v-for="item in list" @click="demo = item">{{item}}</tab-item>
        <!--<tab-item :selected="demo2 === item" v-for="item in list2" @click="demo2 = item">{{item}}</tab-item>-->
      </tab>
    </sticky>
    <br v-for="i in 100">
  </div>
</template>
<style>
  body {
    background-color: yellow;
  }
</style>
<script>
  import Sticky from '../vux/components/sticky/index.vue'
  import Tab from '../vux/components/tab/tab.vue'
  import TabItem from '../vux/components/tab/tab-item.vue'
  export default{
    data () {
      return {
        demo: '正在上映',
        list: ['正在上映', '即将上映']
      }
//      return {
//        demo2: '美食',
//        list2: ['精选', '美食', '电影', '酒店', '外卖']
//      }
    },
    components: {
      Sticky,
      Tab,
      TabItem
    }
  }
</script>
