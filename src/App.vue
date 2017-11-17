<template lang='pug'>
#app
    div 路由列表:<br/>
    router-link(to='/') Mock页面 <br/>
    router-link(to='/hello') Hello页面 <br/>
    router-view
</template>

<script>
export default {
    name: 'app'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
