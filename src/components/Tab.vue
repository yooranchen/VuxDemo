<template>
  <div>
    <!--<tab :line-width="2" active-color="#fc378c">-->
    <!--<tab-item :selected="demo2 === item" v-for="item in list2"-->
    <!--!onclick="demo2 = item" v-show="item">-->
    <!--{{item}}-->
    <!--</tab-item>-->
    <!--</tab>-->
    <tab :line-width="2" active-color="#fc378c" :animate="false">
      <tab-item :selected="demo2 === item" v-for="item in list2" @click="demo2 = item"></tab-item>
    </tab>
  </div>
</template>
<style>

</style>
<script>
  import Tab from '../vux/components/tab/tab.vue'
  import TabItem from '../vux/components/tab/tab-item.vue'
  export default {
    data () {
      return {
        demo2: '美食',
        list2: ['精选', '美食', '电影', '酒店', '外卖']
      }
    },
    components: {
      Tab,
      TabItem
    }
  }
</script>
