<template>
  <div class="box">
    <div class="left">
      <!-- photo -->
      <div class="left_top">
        <div class="card photo_card">
          <p class="title">Photo</p>
          <div class="photo_box">
            <img class="photo_img" src="@/assets/img/myfont.png" alt="">
          </div>
        </div>
      </div>
      <!-- mail -->
      <div class="left_bottom">
        <div class="card mail_box">
          <p class="title" @click="att()">Mail</p>
          <div class="photo_box">
            <img src="@/assets/img/mymail.png" alt="">
            <p class="card_p">web_wuxian@163.com</p>
          </div>
        </div>
      </div>
    </div>
    <div class="center">
      <!-- about me -->
      <div class="center_top">
        <div class="card">
          <p class="title" @click="att()">About Me</p>
        </div>
      </div>
      <div class="center_bottom">
        <!-- github -->
        <div class="center_bottom_box" style="margin-right: 10px">
          <div class="card git_box">
            <p class="title" @click="att()">GitHub</p>
            <div class="photo_box">
              <img src="@/assets/img/mygit.png" alt="">
              <a class="card_p" href="https://github.com/Xu-Jie">https://github.com/Xu-Jie</a>
            </div>
          </div>
        </div>
        <!-- wechart -->
        <div class="center_bottom_box">
          <div class="card chart_box">
            <p class="title" @click="att()">WeChart</p>
            <div class="photo_box">
              <img class="chart_img" src="@/assets/img/mychart.jpg" alt="">
              <p class="card_p">jj1776338251</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="right">
      <!-- where -->
      <div class="right_top">
        <div class="card where_box">
          <p class="title">Where</p>
          <div class="photo_box">
            <img src="@/assets/img/where.png" alt="">
          </div>
        </div>
      </div>
      <!-- friends -->
      <div class="right_bottom">
        <div class="card friends_box">
          <p class="title" @click="att()">Friends</p>
          <ul class="friends_content">
            <li>
              <div class="li_title">三宝</div>
              <a href="https://github.com/Javison666">前端大佬</a>
            </li>
          </ul>
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
.photo_card {
  background-color: #ffd03f;
}
.photo_box {
  width: 100%;
  height: calc(100% - 40px);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.photo_img {
  width: 60%;
}
.mail_box {
  background-color: #ff98c6;
}
.card_p {
  margin-top: 10px;
  color: #000;
}
.git_box {
  background-color: #817ef8;
}
.chart_box {
  background-color: #2fd2db;
}
.where_box {
  background-color: #2fd2db;
}
.friends_box {
  background-color: #ff98c6;
}
.chart_img {
  width: 122px;
}
.friends_content {
  padding: 30px;
  width: 100%;
  height: calc(100% -40px);
  box-sizing: border-box;
}
.friends_content li {
  display: flex;
  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 40px;
  line-height: 40px;
}
.li_title {
  width: 100px;
  color: #000;
  font-size: 18px;
  font-weight: normal;
}
.friends_content li a {
  font-size: 14px;
  color: #aa6584;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.friends_content li a:hover {
  text-decoration: underline;
}
</style>
