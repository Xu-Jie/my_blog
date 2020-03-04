<template>
  <div id="app">
    <div class="nav">
      <div class="nav_body">
        <ul class="nav_list">
          <li>HOME</li>
        </ul>
        <div class="time">{{ gettime }}</div>
      </div>
    </div>
    <div class="home-layout">
      <router-view/>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Home extends Vue {
  public activeMenu = "";
  public gettime: any = "";
  public mounted() {
    this.refreshSiderMenu();
    // window.refreshSiderMenu = () => {
    // };
    this.currentTime();
  }
  public refreshSiderMenu() {
    this.$nextTick(() => {
      const a = 1;
    });
  }
  // 获取时间
  public getTime() {
    // const yy = new Date().getFullYear();
    // const mm = new Date().getMonth() + 1;
    // const dd = new Date().getDate();
    const hh = new Date().getHours();
    const mf =
      new Date().getMinutes() < 10
        ? "0" + new Date().getMinutes()
        : new Date().getMinutes();
    const ss =
      new Date().getSeconds() < 10
        ? "0" + new Date().getSeconds()
        : new Date().getSeconds();
    this.gettime = hh + ":" + mf + ":" + ss;
  }
  // 时间定时器
  public currentTime() {
    setTimeout(() => {
      this.getTime();
      this.currentTime();
    }, 500);
  }
}
</script>
<style lang="scss" scoped>
.nav {
  height: 36px;
  background-color: #fff;
  border-bottom: 1px solid #000;
}
.nav_body {
  margin: 0 auto;
  width: calc(100% - 120px);
  height: 36px;
}
.nav_list {
  float: left;
  line-height: 36px;
  font-weight: bold;
}
.time {
  float: right;
  line-height: 36px;
  font-weight: bold;
}
.home-layout {
  background: #4456a7;
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  top: 37px;
  overflow: hidden;
  overflow-x: auto;
}
</style>
<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  * {
    backface-visibility: hidden;
  }
}
</style>
