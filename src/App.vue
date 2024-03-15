<script setup>
import LayoutHeader from '@/components/layout/Header.vue';
</script>

<template>
<div class="container">
  <layout-header/>
  <div class="content">
   <router-vue/>
  </div>
</div>
  
</template>

<style lang="scss">
@import "./styles/global.scss";

:root {
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
  line-height: 1.5;
  font-weight: 400;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.content {
  max-width: 1440px;
  margin-left: 250px;
  padding: 30px;
  transition: .2s;
  &_full {
    margin-left: 0;
  }
}
</style>
