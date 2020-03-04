<template>
  <div>
    <div class="login-bg"></div>
    <div class="login-default"></div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({})
export default class Home extends Vue {}
</script>
<style lang="scss" scoped>
.login-bg {
  background-image: url("/static/img/bg.jpg");
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  background-size: cover;
  background-position: center;
  z-index: -1;
}
.row {
  margin-bottom: 12px;
}
.login-default {
  padding-top: 18%;
}
</style>

