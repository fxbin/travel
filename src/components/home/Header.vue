<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe614;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe74b;</span>
            输入城市/景点/游玩主题
        </div>
        <div class="header-right">
            城市
            <span class="iconfont arrow-icon">&#xe75d;</span>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        props: {
            msg: String
        }
    }
</script>

<style lang="stylus" scoped>
    @import "../../assets/styles/varibles.styl"
    /*1rem = html font-size = 50px*/
    .header
        display: flex
        height: .86rem
        background: #00bcd4
        color: #ffffff
        .header-left
            width: .64rem
            float: left
            margin: auto
            .back-icon
                text-align: center
                font-size: .4rem
        .header-input
            flex: 1
            height: .64rem
            line-height: .64rem
            margin-top: .12rem
            margin-left: .2rem
            padding-left: .2rem
            background: #ffffff
            border-radius: .1rem
            color: #cacaca
        .header-right
            width: 1.24rem
            margin: auto
            float: right
            text-align: center
            .arrow-icon
                margin-left -.0.5rem
                font-size: .24rem

</style>