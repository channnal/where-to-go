<template>
    <div>
        <ul v-for="weekend of weekendList" :key="weekend.id">
            <li>
                <img :src="weekend.imgUrl" alt="">
                <p>{{weekend.title}}</p>
                <p>{{weekend.desc}}</p>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name:'Homeweekend',
        data(){
            return{
                weekendList:[{
                    id:'0001',
                    imgUrl:'http://img1.qunarzz.com/sight/source/1811/52/b6776b49d27025.jpg_r_640x214_35ae205c.jpg',
                    title:'美丽普陀山',
                    desc:'人间仙境杭州，佛教圣地普陀山等你来玩！在这里静心接收佛家的洗礼，用心感受佛文化'
                },{
                    id:'0002',
                    imgUrl:'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
                    title:'杭州必打卡',
                    desc:'杭州，前世今生与你有一场美丽约会'
                },{
                    id:'0003',
                    imgUrl:'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
                    title:'承载杭城的历史之地',
                    desc:'饱经沧桑的地方诉述着这座城的段段衷肠'
                }]
            }
        }
    }
</script>

<style scoped>

</style>