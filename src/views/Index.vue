<!-- 首页 -->
<template>
  <div class="bg">
    <el-container>
      <el-header>
        <el-input placeholder="" prefix-icon="el-icon-magic-stick" size="small"></el-input>
        <el-button type="text" style="position:absolute;right: 5%" @click="login">登录</el-button>

        <router-view></router-view>
      </el-header>
      <el-main>
        <img src="../assets/imgs/car.jpg" style="height:100%;width:100%" />
      </el-main>
    </el-container>
  </div>
</template>

<script>
  //这里可以导入其他文件（比如：组件，工具js，第三方插件js，json文件，图片文件等等）
  //例如：import 《组件名称》 from '《组件路径》';

  export default {
    //import引入的组件需要注入到对象中才能使用
    components: {},
    data() {
      //这里存放数据
      return {}
    },
    //监听属性 类似于data概念
    computed: {},
    //监控data中的数据变化
    watch: {},
    //方法集合
    methods: {
      login() {
        this.$router.push({ name: 'login' })
      },
    },
    //生命周期 - 创建完成（可以访问当前this实例）
    created() {},
    //生命周期 - 挂载完成（可以访问DOM元素）
    mounted() {},
    beforeCreate() {}, //生命周期 - 创建之前
    beforeMount() {}, //生命周期 - 挂载之前
    beforeUpdate() {}, //生命周期 - 更新之前
    updated() {}, //生命周期 - 更新之后
    beforeDestroy() {}, //生命周期 - 销毁之前
    destroyed() {}, //生命周期 - 销毁完成
    activated() {}, //如果页面有keep-alive缓存功能，这个函数会触发
  }
</script>
<style scoped>
  html,
  body,
  .el-container {
    /*设置内部填充为0，几个布局元素之间没有间距*/
    padding: 0px;
    /*外部间距也是如此设置*/
    margin: 0px;
    /*统一设置高度为100%*/
    height: 100%;
  }
  .el-input {
    width: 120px;
  }

  .el-header {
    height: 60px;
    line-height: 60px;
  }
  .el-main {
    height: calc(100vh - 60px);
    padding: 0px;
    margin: 0px;
  }
  .bg {
    width: 100%;
    padding: 0px;
    margin: 0px;
    background-position: center;
    height: 100%;
    width: 100%;
    background-size: cover;
    position: fixed;
  }
</style>
