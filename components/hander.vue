<template>
  <div class="body_hand">
    <div class="left">
      晚风吹啊啊
    </div>
    <div class="right">
        <div v-for="item in Object.keys(tabs)" @click="path(item)" class="li">{{item}}</div>
    </div>
  </div>
</template>
<script setup lang="ts">
import Home from "~/pages/home.vue";
import My from '~/pages/my.vue'
import Index from '~/pages/index.vue'
import type {DefineComponent} from "vue";

interface tabsType {
  Home: {
    path: string,
    con: DefineComponent<{}, {}, any>
  },
  my: {
    path: string,
    con: DefineComponent<{}, {}, any>
  },
  index: {
    path: string,
    con: DefineComponent<{}, {}, any>
  },
}

const tabs:tabsType = shallowReactive({
  Home: {
    path:"/home",
    con : Home
  },
  my: {
    path:"/my",
    con : My
  },
  index: {
    path:"/",
    con : Index
  },
})
const path = (type : string):void => {
  navigateTo(`${ tabs[type].path}`)
}
</script>
<style scoped lang="scss">
.body_hand {
  width: 100%;
  height: 100%;
  padding: 0 20px;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  box-shadow: 0 4px 8px #0000001a;
  .left {
    width: 450px;
    height: 100%;
    letter-spacing: 2px;
    font-size: 52px;
    font-weight: 600;
    line-height: 1.7;
    font-family: Heavy, 仓耳渔阳体 W04, Arial, sans-serif;
    color: #6e9bc5;
    font-style: italic;
  }
  .right {
    flex: 1;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    .li {
      margin: 0 20px;
    }
  }
}
</style>