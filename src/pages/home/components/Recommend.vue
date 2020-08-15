<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li
      class="item border-bottom"
      v-for="item of recommendList"
      :key="item.id"
      >
          <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default{
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/d3/d3fecf2c578296bba3.img.jpg_200x200_e5fb63fb.jpg',
        title: '长隆欢乐世界',
        desc: '爱挑战的你怎能错过垂直过山车'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201309/06/a03726324b885c8bc8d65eac.jpg_200x200_109f2c42.jpg',
        title: '广州塔',
        desc: '扭动600米高的小蛮腰'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/1c/1c67791edbe2677b90.img.jpg_200x200_ff903759.jpg',
        title: '珠江夜游',
        desc: '感受羊城夜景的美与魅'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl';
  .title
    margin-top:.2rem
    line-height:.8rem
    background:#eee
    text-indent:.2rem
  .item
    overflow:hidden
    display:flex
    height:1.9rem
    .item-img
      width:1.7rem
      height 1.7rem
      padding:.1rem
    .item-info
      flex:1
      padding:.1rem
      min-width:0
      .item-title
        line-height:.54rem
        font-size:.32rem
        ellipsis()
      .item-desc
        line-height:.4rem
        color:#ccc
        ellipsis()
      .item-button
        line-height:.44rem
        margin-top:.16rem
        background #ff9300
        padding:0 .2rem
        border-radius:.06rem
        color:#fff
</style>
