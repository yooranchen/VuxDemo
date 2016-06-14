<template>
  <div>
    <divider>默认</divider>
    <x-header>This is the page title.</x-header>
    <divider>不显示后退</divider>
    <x-header :left-options="{showBack: false}">do not show Back</x-header>
    <divider>显示右侧更多</divider>
    <x-header :right-options="{showMore: true}">with more menu</x-header>
    <divider>使用 right 插槽</divider>
    <x-header>with right link<a slot="right">Feedback</a></x-header>
    <divider>自动文字截断</divider>
    <x-header>long long long long long long long ong long long long long long long text<a slot="right">Feedback</a>
    </x-header>
    <divider>使用 left 插槽</divider>
    <x-header>with left slot<a slot="left">Close</a></x-header>
    <divider>更改背景颜色</divider>
    <x-header style="background-color:#000;">custom background color</x-header>
  </div>
</template>
<style>
</style>
<script>
  import Divider from '../vux/components/divider'
  import XHeader from '../vux/components/x-header'
  export default{
    components: {
      Divider, XHeader
    }
  }
</script>
