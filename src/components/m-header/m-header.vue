<template>
  <div class="m-header">
    <div class="icon"></div>
    <h1 class="text">Chicken Music</h1>
  </div>
</template>
<script type='text/ecmascript-6'>
export default {
  name: ''
}
</script>
<style scoped lang="stylus">
  @import "~common/stylus/variable"
  @import "~common/stylus/mixin"
  .m-header
    position relative
    height 44px
    text-align center
    color $color-theme
    font-size 0
    .icon
      display inline-block
      vertical-align top
      margin-top 6px
      margin-right 6px
      width 30px
      height 32px
      bg-image('logo')
      background-size 32px 30px
    .text
      display inline-block
      vertical-align top
      height 44px
      line-height 44px
      font-size $font-size-large
</style>
