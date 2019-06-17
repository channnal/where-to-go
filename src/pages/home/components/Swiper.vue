<template>
<div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt=""></swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>

</template>

<script>
    export default {
        name:'HomeSwiper',
        data() {
            return {
                swiperOption: {
                    pagination: '.swiper-pagination',
                    loop:true
                },
                swiperList: [{
                    id:10001,
                    imgUrl:"http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/6ab65be3878a5ea365514cf3a8125fd1.jpg_750x200_7b2fe404.jpg"
                },{
                    id:10002,
                    imgUrl:"http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/d7bbc21db442366a882e04ddc984669a.jpg_750x200_85e640d9.jpg"
                },{
                    id:10003,
                    imgUrl:"http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/87a224d0349d94a11e97f31aa1aba4f5.jpg_750x200_1f78af87.jpg"
                }]
            }
        }
    }
</script>

<style lang="stylus" scoped>
.wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 31.25%
    .swiper-img
        width 100%
</style>