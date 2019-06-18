<template>
    <div class="header">
        <div class="header-left" >
            <div class="iconfont  back-icon">&#xe658;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe63c;</span>
            输入城市/景点/游玩主题
        </div>
        <div class="header-right">
            {{this.city}}
            <span class="iconfont arrow-icon">&#xe65c;</span>
        </div>
    </div>
</template>

<script>
import '../../../assets/styles/iconfont.css'
    export default {
        name:"HomeHeader",
        props:{
            city: String

        }
    }
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
    .header
        color:#FFF
        background:$bgColor
        display:flex
        line-height: .86rem
        .header-left
            width: .64rem
            float:left
            .back-icon
                text-align:center
                font-size:.4rem
        .header-input
            flex:1   
            background: #fff
            border-radius: .1rem
            margin:.12rem
            margin-left:.2rem
            padding-left:.2rem
            line-height:.64rem
            color:#ccc

        .header-right
            width: 1.24rem
            float:right
            text-align:center
            .arrow-icon
                font-size:.24rem
                
</style>