<template>
  <divider>横向的scroller</divider>
  <!--<scroller lock-y :scrollbar-x="false">-->
    <!--<div class="box1">-->
      <!--many many content-->
    <!--</div>-->
  <!--</scroller>-->
</template>
<script>
  import Divider from '../vux/components/divider'
//  import Scroller from '../vux/components/scroller'
  export default {
    components: {
      Divider
//      Scroller
    }
  }
</script>

<style>
  .box1 {
    padding: 30px;
  }
</style>
