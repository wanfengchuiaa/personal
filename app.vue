<template>
  <div class="body">
    <header class="header">
      <Hander/>
    </header>
    <div class="content resetScrollBar">
      <NuxtPage />
    </div>
  </div>
</template>
<script setup lang="ts">
import Hander from "../components/hander.vue";
</script>
<style scoped lang="scss">
.body {
  width: 100%;
  height: 98vh;
  //border: red 1px solid;
  box-sizing: border-box;
  position: relative;
  .header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100px;
    background-color: #fff;
  }
  .content {
    width: 100%;
    height: 100%;
    padding-top: 110px;
    box-sizing: border-box;
    background-color: #f7f7f7;
  }
}
.resetScrollBar {
  overflow: hidden;
  overflow-y: auto;
  &::-webkit-scrollbar { /*滚动条整体样式*/
    width: 4px; /*高宽分别对应横竖滚动条的尺寸*/
    height: 1px;
  }
  &::-webkit-scrollbar-thumb { /*滚动条里面小方块*/
    border-radius: 4px;
    -webkit-box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
    background: rgba(243, 243, 243, 0.75);
  }
  &::-webkit-scrollbar-track { /*滚动条里面轨道*/
    -webkit-box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
    border-radius: 10px;
    background: rgba(255, 255, 255, 0.15);
  }
}
/* 在线链接服务仅供平台体验和调试使用，平台不承诺服务的稳定性，企业客户需下载字体包自行发布使用并做好备份。 */
@font-face {
  font-family: "仓耳渔阳体 W05";font-weight: 400;src: url("//at.alicdn.com/wf/webfont/WaKJuPTD40ft/P5dS6RUg680M.woff2") format("woff2"),
url("//at.alicdn.com/wf/webfont/WaKJuPTD40ft/WrRaPIwk9qCP.woff") format("woff");
  font-display: swap;
}
/* 在线链接服务仅供平台体验和调试使用，平台不承诺服务的稳定性，企业客户需下载字体包自行发布使用并做好备份。 */
@font-face {
  font-family: "仓耳渔阳体 W04";font-weight: 400;src: url("//at.alicdn.com/wf/webfont/WaKJuPTD40ft/cIdcV7Jg308V.woff2") format("woff2"),
url("//at.alicdn.com/wf/webfont/WaKJuPTD40ft/kFeBpcOpfD32.woff") format("woff");
  font-display: swap;
}
</style>


<!--<template>-->
<!--  <div class="box">-->
<!--    <NuxtPage />-->
<!--  </div>-->
<!--</template>-->
<!--<script setup lang="ts">-->
<!--import index from '~/pages/index.vue'-->
<!--</script>-->
<!--<style scoped lang="scss">-->
<!--.box {-->
<!--  width: 100%;-->
<!--  height: 100%;-->
<!--}-->
<!--/* 在线链接服务仅供平台体验和调试使用，平台不承诺服务的稳定性，企业客户需下载字体包自行发布使用并做好备份。 */-->
<!--@font-face {-->
<!--  font-family: "仓耳渔阳体 W05";font-weight: 400;src: url("//at.alicdn.com/wf/webfont/WaKJuPTD40ft/P5dS6RUg680M.woff2") format("woff2"),-->
<!--url("//at.alicdn.com/wf/webfont/WaKJuPTD40ft/WrRaPIwk9qCP.woff") format("woff");-->
<!--  font-display: swap;-->
<!--}-->
<!--/* 在线链接服务仅供平台体验和调试使用，平台不承诺服务的稳定性，企业客户需下载字体包自行发布使用并做好备份。 */-->
<!--@font-face {-->
<!--  font-family: "仓耳渔阳体 W04";font-weight: 400;src: url("//at.alicdn.com/wf/webfont/WaKJuPTD40ft/cIdcV7Jg308V.woff2") format("woff2"),-->
<!--url("//at.alicdn.com/wf/webfont/WaKJuPTD40ft/kFeBpcOpfD32.woff") format("woff");-->
<!--  font-display: swap;-->
<!--}-->
<!--</style>-->
