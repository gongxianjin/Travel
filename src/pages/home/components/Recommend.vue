<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img">
                    <img :src="item.imgUrl" alt="">
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
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1712/16/16dd785ae3e2447ba3.img.jpg_200x200_c0ef018f.jpg',
        title: '标题标题',
        desc: '描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1712/16/16dd785ae3e2447ba3.img.jpg_200x200_c0ef018f.jpg',
        title: '标题标题',
        desc: '描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1712/16/16dd785ae3e2447ba3.img.jpg_200x200_c0ef018f.jpg',
        title: '标题标题',
        desc: '描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述描述'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .title
        margin-top: .2rem
        line-height: .8rem
        background: #eee
        text-indent: .2rem
    .item
        overflow: hidden
        display: flex
        height: 1.9rem
        .item-img
            overflow: hidden
            width: 2rem
            height: 2rem
            padding: .1rem
        .item-info
            flex: 1
            padding: .1rem
            min-width:0
            .item-title
             line-height:.54rem
             font-size: .32rem
             ellipsis()
            .item-desc
             line-height:.4rem
             color:#ccc
             ellipsis()
        .item-button
            line-height: .44rem
            margin-top: .16rem
            background:#ff9300
            padding:0 .2rem
            border-radius:.06rem
            color:#fff
</style>
