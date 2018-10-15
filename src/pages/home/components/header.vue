<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont backicon">&#xe624;</div>
        </div>
        <div class="header-input">
             <span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题</div>
        <div class="header-right">{{this.city}} <span class="iconfont arrow-icon">&#xe6aa;</span></div>
    </div>
</template>
<script>
//  1rem = html font-size = 50px
//     86/100
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>
<style lang="stylus" scoped>
    @import '~styles/varibles.styl';
    .header
      display flex
      line-height .86rem
      background $bgColor
      color #ffffff
      .header-left
        width: .64rem
        float: left
        .backicon
            text-align center
            font-size .4rem
      .header-input
        flex: 1
        background #ffffff
        border-radius: .1rem
        line-height .64rem
        height: .64rem
        margin-top: .12rem
        margin-left: .2rem
        padding-left .2rem
        color: #ccc
      .header-right
        width 1.24rem
        float right
        text-align center
        .arrow-icon
            margin-left -.04rem
            font-size .24rem
</style>
