<template>
<div class="icons">
  <swiper>
    <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="icon of page" :key="icon.id">
            <div class="icon-img">
                <img class="icon-imgcontent" :src="icon.imgUrl" alt="">            
            </div>
            <p class="icon-desc">{{icon.desc}}</p>        
        </div>  
    </swiper-slide>  
  </swiper>
</div>
</template>

<script>
    export default {
        name:"HomeIcons",
        props: {
            list: Array
        },
        computed:{
            pages () {
                const pages = []
                this.list.forEach((icon,index)=>{
                    const page = Math.floor(index/8)
                    if(!pages[page]){
                        pages[page]=[]
                    }
                    pages[page].push(icon)
                })                
                return pages
            }
        }
    }
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';
    .icons >>> .swiper-container
        height 0
        padding-bottom 50%
    .icon
        position relative
        overflow hidden
        float left 
        width 25%
        height 0     //限制高度为一半
        padding-bottom 25%
        .icon-img
            position absolute
            top 0
            left 0 
            right 0 
            bottom .44rem
            box-sizing border-box
            padding .1rem
            .icon-imgcontent
                display block
                margin 0 auto
                height 65%
        .icon-desc
            position absolute 
            left 0
            right 0
            bottom 0
            height 1.5rem
            line-height 1.5rem
            color $darkTextColor
            text-align center
            ellipsis()
</style>