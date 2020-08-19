<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class='banner-img' src="//img1.qunarzz.com/sight/p0/1907/90/903428cd6de6a2c1a3.img.jpg_600x330_4fa0bf12.jpg" />
      <div class="banner-info">
        <div class="banner-title">
          广州融创雪世界
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary
    :imgs="imgs"
    v-show="showGallary"
    @close="handleGallaryClose"
    >
    </common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1907/39/394802bd7fce909fa3.img.jpg_r_800x800_250e62f4.jpg', 'http://img1.qunarzz.com/sight/p0/1907/3d/3deee24945b577b3a3.img.jpg_r_800x800_46dee719.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position:relative
    overflow:hidden
    height:0
    padding-bottom:55%
    .banner-img
      width:100%
    .banner-info
      display:flex
      position:absolute
      left:0
      right:0
      bottom:0
      line-height:.6rem
      color:#fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex:1
        font-size:.32rem
        padding:0 .2rem
      .banner-number
        height:.32rem
        line-height:.32rem
        margin-top:.14rem
        padding:0 .4rem
        border-radius:.2rem
        background:rgba(0, 0, 0, .8)
        font-size:.24rem
        .banner-icon
          font-size:.24rem
</style>
