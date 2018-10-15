<template>
    <div>
        <div class="recommend-title">热销推荐</div>
        <ul>
            <li class="item" v-for="item of recommendList" :key="item.id">
                <img :src="item.imgUrl" class="item-img">
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
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/b6/662fc49d1d26a5a7775cf6b7f8b4ecec.water.jpg_200x200_7dec115f.jpg',
        title: '杭州野生动物世界',
        desc: '杭州野生动物世界手机导游(不含门票)手绘地图、语音讲解、路线推荐'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/b6/662fc49d1d26a5a7775cf6b7f8b4ecec.water.jpg_200x200_7dec115f.jpg',
        title: '杭州野生动物世界',
        desc: '杭州野生动物世界手机导游(不含门票)手绘地图、语音讲解、路线推荐'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/b6/662fc49d1d26a5a7775cf6b7f8b4ecec.water.jpg_200x200_7dec115f.jpg',
        title: '杭州野生动物世界',
        desc: '杭州野生动物世界手机导游(不含门票)手绘地图、语音讲解、路线推荐'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .recommend-title
        margin-top .2rem
        line-height .8rem
        background #eeeeee
        text-text-indent .2rem
    .item
        display flex
        overflow hidden
        height 1.9rem
        .item-img
            width 1.7rem
            height 1.7rem
            padding .1rem
        .item-info
            flex: 1
            padding .1rem
            min-width 0
            .item-title
                line-height .54rem
                font-size .32rem
                ellipsis()
            .item-desc
                line-height .4rem
                color #ccc
                ellipsis()
            .item-button
                margin-top .2rem
                background #ff9300
                padding 0 .1rem
                barder-radius .06rem
</style>
