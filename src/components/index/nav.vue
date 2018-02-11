<template>
  <div class="nav-bar">
    <div class="nav-bar-item" v-for="(item,key) in nav_list" :class="{'checked':checked===key}">
      <i class="iconfont" :class="item.icon"></i>
      <span>{{item.text}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'nav',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      checked:0,
      nav_list:[
        {
          icon:'icon-bi',
          text:'笔',
          component:'pen'
        },
        { 
          icon:'icon-xiaolian',
          text:'笑脸',
          component:'face'
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .nav-bar{
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 65px;
    display: flex;
    border-top: 1px solid #3B9193
  }
  .nav-bar-item{
    flex: 1;
    color: #3B9193;
    display: flex;
    flex-direction: column;
    justify-content: center;
    line-height:1;    
  }
  .nav-bar-item.checked{
    background: #3B9193;
    color: #fff
  }
  .nav-bar-item>i{
    font-size: 20px;
    margin-bottom: 5px;
  }
</style>
