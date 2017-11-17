<template lang='pug'>
ul
    li(v-for='item in newsListShow')
        // {{ newsListShow }}
        div {{ item.title }} <img :src='item.thumbnail_pic_s' class='img'/>
        div {{ item.author_name }} {{ item.date }}

</template>

<script>
export default {
    name: '',
    data () {
        return {
            newsListShow: []
        }
    },
    created () {
        this.setNewsApi()
    },
    methods: {
        setNewsApi () {
            this.$http.post('/news', 'type=top&key=123456')
                .then(res => {
                    console.log(res.data)
                    this.newsListShow = res.data.data
                })
                .catch(error => {
                    console.log(error)
                })
        }
    }
}
</script>

<style lang='stylus'>
ul
    li
        border-bottom 1px solid gray
        div
            img
                width 80px
                height 80px

</style>
