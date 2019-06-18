<template>
    <div>
        <ul v-for="weekend of list" :key="weekend.id">
            <li>
                <img :src="weekend.imgUrl" alt="" class="week-img">
                <p>{{weekend.title}}</p>
                <p>{{weekend.desc}}</p>
            </li>
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