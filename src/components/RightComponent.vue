<template>
    <div class="flex-1/2 p-4">
      <!-- Код для вашего вертикального меню с картинками -->
      <div class="w-full bg-white rounded-lg shadow-md p-4">
        <div class="flex flex-col mt-4">
        <div v-for="menuItem in verticalMenuData" :key="menuItem.id" class="flex items-center mr-4 ">
          <img :src="menuItem.image" alt="Menu Item" class="w-10 h-10 object-cover mb-2 rounded-full mr-2">
          <p class="text-center -mt-2">{{ menuItem.title }}</p>
        </div>
      </div>
      </div>
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent } from 'vue';
  
  export default defineComponent({
    data() {
    return {
      verticalMenuData: [
        {
          id: 1,
          title: 'Дошколята',
          image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
        },
        {
          id: 2,
          title: 'Первый класс',
          image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSiGrj42RteKthge9qoxeV_mxLEHn4qIVc9iS3ju-M_BA&s',
        },
        {
          id: 2,
          title: 'Второй класс',
          image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSiGrj42RteKthge9qoxeV_mxLEHn4qIVc9iS3ju-M_BA&s',
        },
        {
          id: 2,
          title: 'Третий класс',
          image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSiGrj42RteKthge9qoxeV_mxLEHn4qIVc9iS3ju-M_BA&s',
        },
        {
          id: 1,
          title: 'Дошколята',
          image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
        },
        {
          id: 1,
          title: 'Дошколята',
          image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
        },
        {
          id: 1,
          title: 'Дошколята',
          image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
        },
        {
          id: 1,
          title: 'Дошколята',
          image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
        },
        {
          id: 1,
          title: 'Дошколята',
          image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
        },
        {
          id: 1,
          title: 'Дошколята',
          image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
        },
        {
          id: 1,
          title: 'Дошколята',
          image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
        },
        {
          id: 1,
          title: 'Дошколята',
          image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
        },
        // Добавьте другие объекты данных для вертикального меню по аналогии
      ],
    };
  },
  props: {
    item: Object,
  },
  });
  </script>