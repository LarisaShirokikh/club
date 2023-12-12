<template>
    <div class="flex h-screen">
      <!-- Боковая область с картинками -->
      <div class="hidden md:block w-1/2 bg-gradient-to-r from-blue-500 to-blue-700">
        <div class="h-full flex items-center justify-center">
          <!-- Ваши картинки здесь -->
          <img src="https://via.placeholder.com/150" alt="Image 1" class="mx-2 rounded-full" />
          <img src="https://via.placeholder.com/150" alt="Image 2" class="mx-2 rounded-full" />
          <img src="https://via.placeholder.com/150" alt="Image 3" class="mx-2 rounded-full" />
        </div>
      </div>
  
      <!-- Форма регистрации -->
      <form class="flex-grow bg-white p-8 rounded-md shadow-md">
        <h2 class="text-2xl font-semibold mb-6">Регистрация</h2>
  
        <div class="grid grid-cols-2 gap-4">
          <!-- Имя пользователя в клубе -->
          <div class="mb-4">
            <label for="clubUsername" class="block text-gray-600 text-sm font-medium">Имя пользователя в клубе</label>
            <input
              type="text"
              id="clubUsername"
              name="clubUsername"
              class="mt-1 p-2 w-full border rounded-md focus:outline-none focus:border-blue-500"
              placeholder="Введите имя пользователя в клубе"
            />
          </div>
  
          <!-- Фамилия, Имя, Отчество -->
          <div class="mb-4">
            <label for="fullName" class="block text-gray-600 text-sm font-medium">Фамилия, Имя, Отчество</label>
            <input
              type="text"
              id="fullName"
              name="fullName"
              class="mt-1 p-2 w-full border rounded-md focus:outline-none focus:border-blue-500"
              placeholder="Введите Фамилию, Имя, Отчество"
            />
          </div>
        </div>
  
        <!-- Номер телефона -->
        <div class="mb-4">
          <label for="phoneNumber" class="block text-gray-600 text-sm font-medium">Номер телефона</label>
          <input
            type="tel"
            id="phoneNumber"
            name="phoneNumber"
            class="mt-1 p-2 w-full border rounded-md focus:outline-none focus:border-blue-500"
            placeholder="Введите номер телефона"
          />
        </div>
  
        <!-- Электронная почта -->
        <div class="mb-4">
          <label for="email" class="block text-gray-600 text-sm font-medium">Электронная почта</label>
          <input
            type="email"
            id="email"
            name="email"
            class="mt-1 p-2 w-full border rounded-md focus:outline-none focus:border-blue-500"
            placeholder="Введите электронную почту"
          />
        </div>
  
        <!-- Пароль -->
        <div class="mb-4">
          <label for="password" class="block text-gray-600 text-sm font-medium">Пароль</label>
          <input
            type="password"
            id="password"
            name="password"
            class="mt-1 p-2 w-full border rounded-md focus:outline-none focus:border-blue-500"
            placeholder="Введите пароль"
          />
        </div>
  
        <!-- Подтверждение пароля -->
        <div class="mb-4">
          <label for="confirmPassword" class="block text-gray-600 text-sm font-medium">Подтверждение пароля</label>
          <input
            type="password"
            id="confirmPassword"
            name="confirmPassword"
            class="mt-1 p-2 w-full border rounded-md focus:outline-none focus:border-blue-500"
            placeholder="Подтвердите пароль"
          />
        </div>
  
        <!-- Чекбокс с текстом -->
        <div class="mb-4">
          <input type="checkbox" id="agreeTerms" name="agreeTerms" class="mr-2" />
          <label for="agreeTerms" class="text-gray-600 text-sm">
            Я внимательно ознакомлен и полностью согласен с условиями членства в клубе и правилами вступления, изложенными в следующих документах:
            Правила совместных закупок, Соглашение пользователя, Политика конфиденциальности, Обработка персональных данных.
          </label>
        </div>
  
        <!-- Кнопка "Зарегистрироваться" -->
        <button
          type="submit"
          class="bg-blue-500 text-white px-4 py-2 rounded-md hover:bg-blue-600 focus:outline-none focus:bg-blue-600"
        >
          Зарегистрироваться
        </button>
        <p class="mt-4 text-gray-600">
        Уже есть аккаунт? <a href="#" @click.prevent="goToLogin" class="text-blue-500">Войти</a>
      </p>
      </form>
    </div>
  </template>
  
  <script setup>
  // Логика формы регистрации (если необходимо)
  </script>
  