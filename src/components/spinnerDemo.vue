<template>
  <div>
    <group>
      <cell v-for="type in types" :title="type">
        <spinner :type="type"></spinner>
      </cell>
    </group>
  </div>
</template>
<style>
  body {
  }
</style>
<script>
  import Group from '../vux/components/group/index.vue'
  import Cell from '../vux/components/cell/index.vue'
  import Spinner from '../vux/components/spinner/index.vue'
  export default{
    data () {
      return {
        types: ['android', 'ios', 'ios-small', 'bubbles', 'circles', 'crescent', 'dots', 'lines', 'ripple', 'spiral']
      }
    },
    components: {
      Group, Cell, Spinner
    }
  }
</script>
