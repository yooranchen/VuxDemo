<template>
  <div>
    <swiper :list="list" auto></swiper>
  </div>
</template>
<style>
</style>
<script>
  import Swiper from '../vux/components/swiper/index.vue'
  export default{
    data () {
      return {
        list: [
          {
            url: 'http://mp.weixin.qq.com/s?__biz=MzAxNjU0MDYxMg==&ampmid=400385458&ampidx=1&ampsn=78f6b8d99715384bdcc7746596d88359&ampscene=19#wechat_redirect',
            img: 'http://7xqzw4.com2.z0.glb.qiniucdn.com/1.jpg',
            title: '如何手制一份秋意的茶？'
          }, {
            url: 'http://mp.weixin.qq.com/s?__biz=MzAxNjU0MDYxMg==&ampmid=400160890&ampidx=1&ampsn=29ef02af25793a11a3f6aec92bfb46c1&ampscene=19#wechat_redirect',
            img: 'http://7xqzw4.com2.z0.glb.qiniucdn.com/2.jpg',
            title: '茶包VS原叶茶'
          }, {
            url: 'http://mp.weixin.qq.com/s?__biz=MzAxNjU0MDYxMg==&ampmid=400094682&ampidx=1&ampsn=8231a2053b772b2108784fccc254d28c&ampscene=19#wechat_redirect',
            img: 'http://7xqzw4.com2.z0.glb.qiniucdn.com/3.jpg',
            title: '播下茶籽，明春可发芽？'
          }
        ]
      }
    },
    components: {Swiper}
  }
</script>
