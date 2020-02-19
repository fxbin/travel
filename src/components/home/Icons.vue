<template>
    <div class="icons">
        <swiper :options="swiperOption">
            <swiper-slide v-for="(page, index) in pages" :key="index">
                <div class="icon" v-for="icon in page" :key="icon.id">
                    <div class="icon-img">
                        <img class="icon-img-content"
                             :src="icon.imgUrl" :alt="icon.desc">
                    </div>
                    <p class="icon-desc">{{icon.desc}}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
    name: "HomeIcons",
    data () {
        return {
            swiperOption: {
                autoplay: false
            },
            icons: [
                {
                    id: '1',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                    desc: '景点门票'
                },
                {
                    id: '2',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fc/b10a6b2e4f0fe102.png',
                    desc: '万龙滑雪'
                },
                {
                    id: '3',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
                    desc: '故宫'
                },
                {
                    id: '4',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fc/b10a6b2e4f0fe102.png',
                    desc: '静之湖滑雪'
                },
                {
                    id: '5',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                    desc: '一日游'
                },
                {
                    id: '6',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png',
                    desc: '古北水镇'
                },
                {
                    id: '7',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fc/b10a6b2e4f0fe102.png',
                    desc: '北京滑雪'
                },
                {
                    id: '8',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fc/b10a6b2e4f0fe102.png',
                    desc: '陶然亭滑雪'
                },
                {
                    id: '9',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
                    desc: '泡温泉'
                },
                {
                    id: '10',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png',
                    desc: '中国马镇'
                }

            ]
        }
    },
    computed: {
        pages () {
            const pages = []
            this.icons.forEach((item, index) => {
                const page = Math.floor(index / 8)
                if (!pages[page]) {
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import "../../assets/styles/varibles.styl"
    @import "../../assets/styles/mixins.styl"

    .icons >>> .swiper-container
        margin-top: .1rem
        height: 0
        padding-bottom: 50%
    .icon
        position: relative
        float: left
        width: 25%
        height: 0
        padding-bottom: 25%
        .icon-img
            position: absolute
            top: 0
            left: 0
            right: 0
            bottom: .44rem
            box-sizing: border-box
            padding: .1rem
            .icon-img-content
                display: block
                margin: 0 auto
                height: 100%
        .icon-desc
            position: absolute
            left: 0
            right: 0
            bottom: 0
            height: .44rem
            line-height: .44rem
            text-align: center
            color: $darkTextColor
            ellipsis()

</style>