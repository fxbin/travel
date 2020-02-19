<!-- The ref attr used to find the swiper instance -->
<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="banner in banners" :key="banner.id">
                <img class="swiper-img" :src="banner.imgUrl" alt=""/>
            </swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeSwiper',
    data () {
        return {

            swiperOption: {
                pagination: {
                    el: '.swiper-pagination'
                },
                loop: true
            },
            banners: [
                {
                    id: '1',
                    imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20201/be6871c9b0b0ffab3ef2a86fa9688677.jpg'
                },
                {
                    id: '2',
                    imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/0b26e9760c2673c63c05e1efce1275ea.jpg_750x200_495c0a72.jpg'
                }
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background: #ffffff
    .wrapper
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom: 26.5%
        background-color: #cacaca
    .swiper-img
        width: 100%

</style>