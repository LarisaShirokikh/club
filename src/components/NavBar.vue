<script setup lang="ts">
import { ref, computed } from 'vue';

const isLoggedIn = ref(/* логика проверки залогинен ли пользователь */);
const userNickname = ref(/* никнейм пользователя, если есть */);
const userAvatar = ref(/* URL аватарки пользователя, если есть */);
const showProfileMenu = ref(false);

// Функции для работы с профилем
const toggleProfileMenu = () => {
  showProfileMenu.value = !showProfileMenu.value;
};

const toggleNotifications = () => {
  // Логика отображения уведомлений
};

const openSettings = () => {
  // Логика открытия настроек
};

const logout = () => {
  // Логика выхода из системы
};
</script>

<template>
    <nav class=" p-2 flex items-center">
      <a href="#/" class="text-gray-500 mx-2 px-4 py-2">Главная</a>
      <a href="#/news" class="text-gray-500 mx-2 px-4 py-2">Новости</a>
      <a href="#/forum" class="text-gray-500 mx-2 px-4 py-2">Форум</a>
     
     
      <div class="relative">
  <input
    type="text"
    placeholder="Поиск..."
    class="border px-4 py-1 rounded-md focus:outline-none w-64"
  />
  <button class="absolute right-0 top-1/2 transform -translate-y-1/2 text-gray-500 mr-3 focus:outline-none">
    <!-- Иконка поиска -->
    <Search style="width: 1em; height: 1em; margin-right: 5px" />
  </button>
</div>

 <!-- Контент для залогиненного пользователя -->
 <div v-if="isLoggedIn" class="flex items-center text-gray-500 ml-auto">
      <button class="ml-4" @click="toggleNotifications">
        <!-- Иконка колокольчика (замените на вашу иконку) -->
        <Bell style="width: 1.5em; height: 1.5em; margin-right: 5px" />
      </button>
      <button class="ml-4" @click="openSettings">
        <!-- Иконка флажка (замените на вашу иконку) -->
        <Setting style="width: 1.5em; height: 1.5em; margin-right: 5px" />
      </button>

    <div class="flex items-center ml-4" @click="toggleProfileMenu">
        <!-- Иконка аватарки (замените на вашу иконку) -->
    <img 
    src="https://www.svgrepo.com/show/382100/female-avatar-girl-face-woman-user-7.svg" 
    alt="Avatar" 
    class="w-8 h-8 rounded-full">
  <!-- Выводим никнейм пользователя, если он есть -->
  <span v-if="userNickname" class="ml-2">{{ userNickname }}</span>
        <!-- Иконка шестеренки -->
        <button @click="toggleProfileMenu">
          <Gear size="1.5em" style="margin-left: 5px; cursor: pointer;" />
        </button>
        <!-- Всплывающее меню для профиля -->
        <div v-if="showProfileMenu" class="absolute right-0 mt-2 bg-white border rounded-md shadow-md">
          <router-link to="/profile" class="block px-4 py-2">Профиль</router-link>
          <router-link to="/settings" class="block px-4 py-2">Настройки</router-link>
          <button @click="logout" class="block px-4 py-2 text-red-500">Выйти</button>
        </div>
      </div>
    </div>

    <!-- Контент для не залогиненного пользователя -->
    <div v-else class="flex items-center text-gray-500 ml-auto">
      <router-link to="/login" class="ml-4">Войти</router-link>
      <router-link to="/register" class="ml-4">Регистрация</router-link>
    </div>
  </nav>
</template>