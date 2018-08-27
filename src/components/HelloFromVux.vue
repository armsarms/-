<template>
  <div>
    <div class="vux-demo">
      <img class="logo" src="../assets/vux_logo.png">
      <h1></h1>
    </div>
    <group title="cell demo">
      <cell title="VUX" value="cool" is-link></cell>
    </group>
    <div id="myMap"></div>
  </div>
</template>
<script>
import AMap from 'AMap';   //在页面中引入高德地图
import { Group, Cell } from 'vux'
export default {
   mounted(){
       this.loadmap();     //加载地图和相关组件
    },
    methods: {
      loadmap(){
        const map = new AMap.Map('myMap', {
          zoom: 9
        });
      }
    },
  components: {
    Group,
    Cell
  },
  data () {
    return {
      // note: changing this line won't causes changes
      // with hot-reload because the reloaded component
      // preserves its current state and we are modifying
      // its initial state.
      msg: 'Hello World!'
    }
  }
}
// var map = new AMap.Map('myMap', {
//         zoom:11,//级别
//         center: [116.397428, 39.90923],//中心点坐标
//         viewMode:'3D'//使用3D视图
//     });
</script>

<style>
.vux-demo {
  text-align: center;
}
.logo {
  width: 100px;
  height: 100px
}
#myMap {
  width: 100%;
  height: 300px;
}
</style>
