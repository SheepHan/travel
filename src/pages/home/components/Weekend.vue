<template>
  <div>
      <div class="recommend-title">周末去哪儿</div>
      <ul>
          <li class="item border-bottom" v-for="item of list" :key="item.id">           
              <div class="img-wrapper">
                <img :src="item.imgUrl" alt="" class="item-img"> 
              </div>   
                              
              <div class="item-info">
                  <p class="item-title">{{item.title}}</p>
                  <p class="item-desc">{{item.desc}}</p>
              </div>
          </li>
      </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  props: {
      list: Array
  }
}
</script>
<style lang="stylus" scoped>
    .recommend-title
        line-height .8rem
        background #eeeeee
        text-indent .2rem
    .img-wrapper
        overflow hidden
        height 0
        padding-bottom 37.9%
        .item-img
            width 100%
    .item-info
        padding .1rem
        min-width 0
        .item-title
            line-height .54rem
            font-size .32rem   
        .item-desc
            line-height .4rem
            color: #cccccc
</style>
