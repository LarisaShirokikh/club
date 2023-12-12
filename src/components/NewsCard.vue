<template>
    <div class="flex space-x-4 overflow-x-auto p-4 overflow-x-hidden" @wheel="handleScroll">
      <div v-for="news in newsList" 
      :key="news.id"
      class="flex-none w-64 bg-white rounded-lg shadow-md overflow-hidden">
        <img :src="news.image" alt="News Image" class="w-full h-32 object-cover">
        <div class="p-4">
          <h2 class="text-xl font-semibold">{{ news.title }}</h2>
          <p class="text-gray-600">{{ news.description }}</p>
        </div>
      </div>
    </div>
  </template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  props: {
    newsList: {
      type: Array,
      required: true,
    },
  },
  methods: {
    handleScroll(event: WheelEvent) {
      const container = event.currentTarget as HTMLElement;
      const delta = event.deltaY || event.deltaX;

      container.scrollLeft += delta;
    },
  },
});
</script>