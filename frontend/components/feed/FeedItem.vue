<template>
  <div
    class="p-2 border rounded-md bg-light-header dark:bg-dark-header border-light-section-div dark:border-dark-section-div sm:p-3 shadow-sm shadow-zinc-700"
  >
    <div class="flex items-center space-x-3">
      <Icon v-if="(item.itemType = 'group')" name="bi:people" size="1.5em" />
      <Icon
        v-else-if="item.url.includes('mastodon')"
        name="bi:mastodon"
        size="1.5em"
      />
      <Icon
        v-else-if="item.url.includes('facebook')"
        name="bi:facebook"
        size="1.5em"
      />
      <Icon
        v-else-if="item.url.includes('instagram')"
        name="bi:instagram"
        size="1.5em"
      />
      <h4 class="font-bold responsive-h5">{{ item.title }}</h4>
    </div>
    <p class="pb-3">
      {{ item.description }}
    </p>
    <div
      class="w-full h-32 rounded-md bg-light-placeholder dark:bg-dark-placeholder"
    >
      <img :src="item.imgURL" alt="" />
    </div>
  </div>
</template>

<script setup lang="ts">
import type { FeedItem } from "../../types/feedItem";

const props = defineProps<{
  url: string;
}>();

let itemType: string = "";
if (props.url.includes("activist")) {
  itemType = "group";
} else {
  itemType = "social post";
}

const item: FeedItem = {
  url: props.url,
  itemType: itemType,
  title: "Title",
  description: "Lorem ipsum dolor sit amet",
};
</script>
