<template>
  <SidebarRightHamburger
    @toggle="toggleMenuState"
    class="flex items-center h-full"
    ref="ignoreElRef"
    :menuOpen="menuOpen"
  />
  <div
    class="fixed top-0 right-0 z-40 h-screen pt-12 overflow-y-auto border-l bg-light-distinct transition-[max-width] overflow-x-hidden duration-200 border-light-section-div dark:bg-dark-distinct dark:border-dark-section-div shadow-sm shadow-zinc-700"
    :class="{
      'max-w-0 px-0': !menuOpen,
      'max-w-[16rem] px-4': menuOpen,
    }"
    ref="target"
    id="drawer-navigation"
    tabindex="-1"
  >
    <div
      class="w-56 h-full py-4"
      :class="{
        hidden: !menuOpen,
      }"
    >
      <slot></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
import { onClickOutside } from "@vueuse/core";
import { ref } from "vue";

const target = ref();
const menuOpen = ref(false);
const ignoreElRef = ref();

const toggleMenuState = () => {
  menuOpen.value = !menuOpen.value;
};

onClickOutside(
  target,
  () => {
    if (!menuOpen.value) return;
    toggleMenuState();
  },
  { ignore: [ignoreElRef] }
);
</script>
