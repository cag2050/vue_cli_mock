<template>
<div>mock</div>
</template>

<script>
export default {
    name: '',
    data () {
        return {
            msg: 'Welcome to Your Vue.js App'
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
                    // this.newsListShow = res.data.data;
                })
                .catch(error => {
                    console.log(error)
                })
        }
    }
}
</script>

<style scoped>

</style>
