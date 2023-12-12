<script setup lang="ts">
import { computed, defineComponent, ref } from 'vue';

import NavBar from './components/NavBar.vue';
import MainCom from './components/MainCom.vue'
import Login from './components/loginPage.vue';
const isUserLoggedIn = ref(true);

const currentComponent = computed(() => {
  // Определите, какой компонент отображать в зависимости от состояния авторизации
  return isUserLoggedIn.value ? MainCom : Login;
});

const showLogin = () => {
  // Логика показа компонента Login
  isUserLoggedIn.value = false;
};

const showRegister = () => {
  // Логика показа компонента Регистрации
  isUserLoggedIn.value = false;
};

const newsData = [
  {
    id: 1,
    title: 'Заголовок новости 1',
    description: 'Описание новости 1',
    image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
  },
  {
    id: 2,
    title: 'Заголовок новости 2',
    description: 'Описание новости 2',
    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSiGrj42RteKthge9qoxeV_mxLEHn4qIVc9iS3ju-M_BA&s',
  },
  {
    id: 2,
    title: 'Заголовок новости 2',
    description: 'Описание новости 2',
    image: 'https://img.freepik.com/free-photo/a-cupcake-with-a-strawberry-on-top-and-a-strawberry-on-the-top_1340-35087.jpg',
  },
  {
    id: 2,
    title: 'Заголовок новости 2',
    description: 'Описание новости 2',
    image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
  },
  {
    id: 2,
    title: 'Заголовок новости 2',
    description: 'Описание новости 2',
    image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
  },
  {
    id: 2,
    title: 'Заголовок новости 2',
    description: 'Описание новости 2',
    image: 'https://i.pinimg.com/236x/2a/f5/3d/2af53d8f1be483dd0e05b7b18142c33c.jpg',
  },
  // Добавьте другие новости по аналогии
];


</script>

<template>
  <div>
    <NavBar/>
    <component :is="currentComponent" class="" />
    <!-- <NewsCard :newsList="newsData" class="mt-3"/> -->
    <!-- <MainCom class=""/> -->
  </div>
</template>

<style scoped>
/* Ваши стили здесь */
</style>
