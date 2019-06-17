<template>
    <div>
        <ul v-for="recommend in recommendList" :key="recommend.id">
            <div class="title">{{recommend.title}}</div>
            <li class="">
                <img :src="recommend.imgUrl" alt="">
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name:'HomeRecommend',
        data() {
            return {
                recommendList: [{
                    id:'001',
                    imgUrl:'http://img1.qunarzz.com/sight/p0/1904/a2/a23ae48aac0c0ab2a3.water.jpg_200x200_38cef490.jpg',
                    title:'西溪国家湿地洪园',
                    desc:''
                },{
                    id:'002',
                    imgUrl:'http://img1.qunarzz.com/sight/p0/1903/e0/e0e0c6ca274ad49aa3.img.jpg_200x200_0f072efb.jpg',
                    title:'西溪国家湿地洪园·周家村',
                    desc:''
                },{
                    id:'003',
                    imgUrl:'http://img1.qunarzz.com/sight/p0/1810/cc/cc47164357acbeb5a3.water.jpg_200x200_151f0405.jpg',
                    title:'杭州云曼温泉',
                    desc:''
                }]
            }
        }
    }
</script>

<style lang="stylus" scoped>

</style>