<template>
  <div class="flex-col w-full h-screen overflow-y-auto overflow-hidden p-4">
    <div v-for="post in postList" :key="post.id" class="flex-none w-full bg-white rounded-lg shadow-md mb-4">
      <!-- Информация о пользователе -->
      <div class="flex items-center p-2 text-sm text-gray-500">
        <img :src="post.user.avatar" alt="User Avatar" class="w-8 h-8 rounded-full mr-2">
        <span>{{ post.user.name }}</span>
        <span>&bull;</span>
        <span>{{ timeAgo(post.createdAt) }}</span>
      </div>
      
      <!-- Заголовок поста -->
      <h2 class="text-xl font-semibold p-2">{{ post.title }}</h2>
      
      <!-- Информация о просмотрах -->
      <div class="flex items-center p-2 text-sm text-gray-500">
        <View style="width: 1em; height: 1em; margin-right: 8px" />
        <span>{{ post.views }} просмотров</span> 
      </div>
      
      <!-- Рубрики -->
      <div class="flex items-center p-2">
        <span v-for="category in post.categories" :key="category.id" class="mr-2 text-blue-500 cursor-pointer">{{ category.name }}</span>
      </div>
      
      <!-- Фото и краткое превью текста -->
      <img :src="post.image" alt="Post Image" class="w-full h-80 object-cover rounded-b-lg">
      <div class="p-2">
        <p class="text-gray-600">{{ post.previewText }}</p>
        <p class="text-blue-500 cursor-pointer">Читать далее...</p>
      </div>

      <!-- Иконки и количество действий (лайки, сохранение, комментарии, переслать) -->
      <div class="flex items-center p-2 text-gray-500">
        <Star style="width: 1em; height: 1em; margin-right: 8px" />
        {{ post.likes }}
        <ChatRound style="width: 1em; height: 1em; margin-right: 8px" />
        {{ post.saved }}
        <CollectionTag style="width: 1em; height: 1em; margin-right: 8px" />
        {{ post.comments }}
        <Position style="width: 1em; height: 1em; margin-right: 8px" />
        {{ post.forwards }}
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">


const props = defineProps(['postList']);

// Пример функции для отображения времени в прошлом
const timeAgo = (timestamp) => {
  // Ваша логика расчета времени
  return '2 часа назад'; // Пример
};
</script>
