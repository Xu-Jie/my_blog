<template>
  <div class="box">
    <div class="left">
      <div class="left_top">
        <div class="card">
          <p class="title">Photo</p>
        </div>
      </div>
      <div class="left_bottom">
        <div class="card">
          <p class="title" @click="att()">Photo</p>
        </div>
      </div>
    </div>
    <div class="center">
      <div class="center_top">
        <div class="card">
          <p class="title" @click="att()">Photo</p>
        </div>
      </div>
      <div class="center_bottom">
        <div class="center_bottom_box" style="margin-right: 10px">
          <div class="card">
            <p class="title" @click="att()">Photo</p>
          </div>
        </div>
        <div class="center_bottom_box">
          <div class="card">
            <p class="title" @click="att()">Photo</p>
          </div>
        </div>
      </div>
    </div>
    <div class="right">
      <div class="right_top">
        <div class="card">
          <p class="title">Photo</p>
        </div>
      </div>
      <div class="right_bottom">
        <div class="card">
          <p class="title" @click="att()">Photo</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Home extends Vue {
  // public att() {
  //   this.$store.dispatch("user/updateNum", "2")
  // }
}
</script>
<style lang="scss" scoped>
.box {
  margin: 0 auto;
  margin-top: 15px;
  width: calc(100% - 120px);
  height: 98%;
  display: flex;
}
.left {
  flex: 1;
  margin: 0 5px;
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  height: 100%;
}
.left_top {
  position: relative;
  height: 64%;
  margin-bottom: 15px;
}
.left_bottom {
  height: 33%;
}
.card {
  border-radius: 15px;
  border: 1px solid #000;
  height: 100%;
  font-weight: bold;
  overflow: hidden;
  .title {
    line-height: 40px;
    border-bottom: 1px solid #000;
    background-color: #fff;
  }
}
.center {
  flex: 2;
  margin: 0 5px;
  height: 100%;
}
.center_top {
  flex: 1;
  height: 64%;
  margin-bottom: 15px;
}
.center_bottom {
  flex: 1;
  display: flex;
  height: 33%;
}
.center_bottom_box {
  flex: 1;
  height: 100%;
}
.right {
  flex: 1;
  margin: 0 5px;
  height: 100%;
}
.right_top {
  position: relative;
  height: 33%;
  margin-bottom: 15px;
}
.right_bottom {
  height: 64%;
}
</style>
