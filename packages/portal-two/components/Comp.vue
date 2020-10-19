<template>
  <PortalOneComp class="overridden" />
</template>
<style>
.overridden {
  text-transform: uppercase;
}
</style>
<script>
// 為了避免因為使用 nuxt.config.js 內設定的 components: true, 自動 import 命名衝突
// 本地若有相同名稱的組件, 需要用以下方式更改名稱, 避免出現自己 import 自己的無限循環 Maximum call stack size exceeded 報錯
// import Comp from "portal-one/components/Comp.vue"; // error!
import PortalOneComp from "portal-one/components/Comp.vue";

export default {
  name: "Comp",
  components: { PortalOneComp }
};
</script>