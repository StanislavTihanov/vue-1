<script setup>
import { ref } from "vue";

const props = defineProps({
  openSidebar: {
    type: Boolean,
    required: true,
  },
});

const links = ref([
  { name: "Typography", href: "/typography" },
  { name: "Button", href: "/button" },
]);
</script>

<template>
  <div :class="['sidebar', { sidebar_isopen: openSidebar }]">
    <router-link
      class="sidebar__link"
      v-for="link in links"
      :key="link.name"
      :to="link.href"
      >{{ link.name }}</router-link
    >
  </div>
</template>

<style lang="scss" scoped>
.sidebar {
  top: 62px;
  left: 0;
  height: 100%;
  background: #fff;
  position: fixed;
  width: 250px;
  padding: 20px;
  transition: 0.2s;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.07);
  transform: translateX(-250px);
  &_isopen {
    transform: translateX(0px);
  }
  &__link {
    display: block;
    border-radius: 12px;
    padding: 10px;
    border: 2px solid #fff;
    transition: 0.2s;
    font-weight: bold;
    margin-bottom: 10px;
    &:hover {
      border-color: var(--primary);
    }
  }
}
</style>