<template>
  <div id="app">
    <!--<router-view></router-view>-->
      <div class="fake-title-bar">
      Menu
        <div class="handle-bar" v-if="os === 'win32'"> <!-- 如果是windows系统 就加上模拟的操作按钮-->
          <i class="el-icon-minus" @click="minimizeWindow"></i>
          <i class="el-icon-close" @click="closeWindow"></i>
        </div>
      </div>

      <div class="tool-card">
        countdown
      </div>

  </div>
</template>

<script>
  export default {
    name: 'y',
  };
</script>

<style>
  .fake-title-bar {
    -webkit-app-region: drag;
    background-color: rgb(198, 82, 112);
  }
  .handle-bar {
    -webkit-app-region: no-drag;
  }
  .tool-card {
    width:180px;
    height:180px;
    background-color: rgb(70, 203, 187);
    color: #ffffff;
    border-right: 10px solid #fff;
    border-top: 10px solid #fff;
  }
</style>
