<template>
  <div>
    <group>
      <switch title="default popup" :value.sync="show"></switch>
      <switch title="full poupo" :value.sync="show1"></switch>
    </group>
    <popup :show.sync="show">
      <div class="popup0">
        <group>
          <switch title="Anthoer Switcher" :value.sync="show"></switch>
        </group>
      </div>
    </popup>
    <popup :show.sync="show1" height="100%">
      <div class="popup1">
        <group>
          <switch title="Another Switcher" :value.sync="show1"></switch>
        </group>
      </div>
    </popup>
  </div>
</template>
<script>
  import Group from '../vux/components/group/index.vue'
  import Switch from '../vux/components/switch/index.vue'
  import Popup from '../vux/components/popup/index.vue'
  export default {
    data () {
      return {
        show: false,
        show1: false
      }
    },
    components: {
      Group,
      Switch,
      Popup
    }
  }
</script>
<style>
  .popup0 {
    padding-bottom: 15px;
    height: 200px;
  }

  .popup1 {
    width: 100%;
    height: 100%;
  }
</style>
