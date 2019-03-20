<template>
  <div id="app" @touchmove.prevent>
    <m-header></m-header>
    <tab></tab>
    <keep-alive>
      <router-view class="router"></router-view>
    </keep-alive>
  </div>
</template>

<script type="text/ecmascript-6">
import MHeader from 'components/m-header/m-header'
import Tab from 'components/tab/tab'
export default {
  name: '',
  components: {
    MHeader,
    Tab
  }
}
</script>
<style scoped lang="stylus" rel="stylesheet/stylus">
  @import '~common/stylus/variable';
    .router
      color $color-theme-d
</style>