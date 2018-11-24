<template>
  <div class="dashboard-container">
    hello world
    {{name}}
  </div>
</template>

<script>
  import {mapGetters} from 'vuex'
  import {getInfo} from '../../api/login.js'
  export default {
    name: 'dashboard',
    computed: {
        name(){
            return this.$route.path
        }
    },
    mounted:{
      getInfo().then(function(response){
        alert(response);
      })
    }
  }
</script>

<style rel="stylesheet/less" lang="less">
</style>
