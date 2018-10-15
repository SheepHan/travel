<template>
    <div>
        <div class="recommend-title">周末去哪儿</div>
        <ul>
            <li class="item" v-for="item of recommendList" :key="item.id">
                <div class="item-img-warpper">
                    <img :src="item.imgUrl" class="item-img">
                </div>
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
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
        title: '杭州野生动物世界',
        desc: '杭州野生动物世界手机导游(不含门票)手绘地图、语音讲解、路线推荐'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
        title: '杭州野生动物世界',
        desc: '杭州野生动物世界手机导游(不含门票)手绘地图、语音讲解、路线推荐'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
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
    .item-img-warpper
        overflow hidden
        height 0
        padding-bottom 28%
        .item-img
            width 100%
    .item-info
        padding .1rem
        .item-title
            line-height .54rem
            font-size .32rem
            ellipsis()
        .item-desc
            line-height .4rem
            color #ccc
            ellipsis()
</style>