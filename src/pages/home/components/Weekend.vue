<template>
    <div>
            <div class="title">周末去哪儿</div>

        <ul>
            <router-link tag="li" :to="/detail/+weekend.id" class="item border-bottom" v-for="weekend of list" :key="weekend.id" >
                <img :src="weekend.imgUrl" alt="" class="week-img">
                <p>{{weekend.title}}</p>
                <p>{{weekend.desc}}</p>
            </router-link>

        </ul>
    </div>
</template>

<script>
    export default {
        name:'Homeweekend',
        props: {
            list:Array,
            title:String
        }
    }
</script>

<style lang="stylus" scoped>
    .week-img
        width 100%
</style>