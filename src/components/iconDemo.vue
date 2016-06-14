<template>
  <div>
    <icon type="success"></icon>
    <icon type="info"></icon>
    <icon type="info_circle"></icon>
    <icon type="warn"></icon>
    <icon type="waiting"></icon>
    <icon type="waiting_circle"></icon>
    <icon type="safe_success"></icon>
    <icon type="safe_warn"></icon>
    <icon type="success_circle"></icon>
    <icon type="success_no_circle"></icon>
    <icon type="circle"></icon>
    <icon type="download"></icon>
    <icon type="cancel"></icon>
    <icon type="search"></icon>
    <icon type="clear"></icon>
    <br/>
    <icon type="success" class="icon_big"></icon>
    <icon type="info" class="icon_big"></icon>
    <icon type="safe_success" class="icon_big"></icon>
    <icon type="safe_warn" class="icon_big"></icon>
  </div>
</template>
<style>
  .icon_big {
    height: 100px;
    width: 100px;
  }
</style>
<script>
  import Icon from '../vux/components/icon/index.vue'
  export default{
    components: {
      Icon
    }
  }
</script>
