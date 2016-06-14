<template>
  <divider>横向的</divider>
  <flexbox style="height:40px;">
    <flexbox-item>
      <div class="flex-demo">1</div>
    </flexbox-item>
    <flexbox-item>
      <div class="flex-demo">2</div>
    </flexbox-item>
  </flexbox>
  <divider>纵向的</divider>
  <flexbox orient="vertical" :margin-left=0>
    <flexbox-item>
      <div class="flex-demo">1</div>
    </flexbox-item>
    <flexbox-item>
      <div class="flex-demo">2</div>
    </flexbox-item>
  </flexbox>
</template>
<script>
  import FlexBox from '../vux/components/flexbox'
  import Divider from '../vux/components/divider'
  export default {
    components: {
      FlexBox,
      Divider
    }
  }
</script>
<style>
  .flex-demo {
    text-align: center;
    color: #fff;
    background-color: #20b907;
    margin-bottom: 8px;
    border-radius: 4px;
    -webkit-background-clip: padding-box;
  }
</style>
