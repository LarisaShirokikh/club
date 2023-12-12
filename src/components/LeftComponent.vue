<template>
  
    
      <div class="flex flex-col space-y-4">
       
<div>
  <PostCard v-for="post in posts" :key="post.id" :post="post" />
</div>
      </div>
    
  
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import PostCard from './PostCard.vue';

export default defineComponent({
  components: {
    PostCard,
  },
  data() {
    return {
      // Пример данных для постов (замените на свои данные)
      posts: [
        {
          id: 1,
          title: 'Заголовок поста 1',
          description: 'Описание поста 1',
          image: 'url-to-image-1.jpg',
        },
        {
          id: 2,
          title: 'Заголовок поста 2',
          description: 'Описание поста 2',
          image: 'url-to-image-2.jpg',
        },
        // Добавьте другие посты по аналогии
      ],
    };
  },
});
</script>
