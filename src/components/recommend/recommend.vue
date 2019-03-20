<template>
  <div class="recommend">
    <div class="recommend-content">
      <div class="slider-wrapper">
        <slider>
          <div v-for="recommend in recommends" :key='recommend.id'>
            <a :href="recommend.linkUrl">
              <img :src="recommend.picUrl" alt="">
            </a>
          </div>
        </slider>
      </div>
      <div class="recommend-list">
        <h1 class="list-title">推荐热门歌单</h1>
        <ul></ul>
      </div>
    </div>
  </div>
</template>
<script type="text/ecmascript-6">
import {ERR_OK} from 'api/config'
import {getRecommend, getDescList} from 'api/recommend'
import Slider from 'base/slider/slider'
export default {
  name: '',
  data() {
    return {
      recommends: []
    }
  },
  components: {
    Slider
  },
  created() {
    this._getRecommend()
    this._getDescList()
  },
  methods: {
    _getRecommend() {
      getRecommend().then((res) => {
        if (res.code === ERR_OK) {
          console.log(res.data.slider)
          this.recommends = res.data.slider
        }
      })
    },
    _getDescList() {
      getDescList().then((res) => {
        console.log(res)
      })
    }
  }
}
</script>
<style scoped lang="stylus">

</style>
