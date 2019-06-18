<template>
    <div>
        <ul v-for="recommend in list" :key="recommend.id">
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
        props: {
            title: String,
            list: Array
        }
    }
</script>

<style lang="stylus" scoped>

</style>