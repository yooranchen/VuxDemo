<template>
  <div>
    <timeline :color="color">
      <timeline-item v-for="i in count">
        <h4 :class="[i === 0 ? 'recent' : '']">Timeline Node NaN</h4>
        <p :class="[i === 0 ? 'recent' : '']">index NaN<</p>
      </timeline-item>
    </timeline>
    <x-button @click="count = 6" >Set to 6 item</x-button>
    <x-button @click="count = 3">Set to 3 item</x-button>
  </div>
</template>
<style>
  .timeline-demo p {
    color: #888;
    font-size: 0.8rem;
  }

  .timeline-demo h4 {
    color: #666;
    font-weight: normal;
  }

  .recent {
    color: rgb(4, 190, 2);
  }
</style>
<script>
  import XButton from '../vux/components/x-button/index.vue'
  import Timeline from '../vux/components/timeline/timeline.vue'
  import TimelineItem from '../vux/components/timeline/timeline-item.vue'
  export default{
    data () {
      return {
        color: '#00ff00',
        count: 3
      }
    },
    components: {
      Timeline, TimelineItem, XButton
    }
  }
</script>
