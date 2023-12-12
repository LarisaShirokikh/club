  
  <script lang="ts" setup>
  import { defineComponent } from 'vue';
  import RightComponent from './RightComponent.vue';
  import NewsCard from './NewsCard.vue';
  import PostCard from './PostCard.vue';
  
  
  const postData = [
  {
  id: 1,
  title: 'Заголовок поста 1',
  description: 'Описание поста 1',
  image: 'https://img.freepik.com/free-photo/forest-landscape_71767-127.jpg',
  user: {
    name: 'John Doe',
    avatar: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQD-YTaXf90G-8IWx6llFRzjmm0ctLDUlzwKg&usqp=CAU',
  },
  createdAt: new Date(), // Добавлено поле с датой создания
  views: 1000, // Пример количества просмотров
  categories: [
    { id: 1, name: 'Природа' },
    { id: 2, name: 'Путешествия' },
  ],
  previewText: 'Это краткое описание поста, которое видно в основном блоке.',
  likes: 50, // Пример количества лайков
  saved: 20, // Пример количества сохранений
  comments: 30, // Пример количества комментариев
  forwards: 10, // Пример количества пересылок
},
{
  id: 1,
  title: 'Заголовок поста 1',
  description: 'Описание поста 1',
  image: 'https://img.freepik.com/free-photo/forest-landscape_71767-127.jpg',
  user: {
    name: 'John Doe',
    avatar: 'https://i.pinimg.com/236x/aa/17/14/aa17142ab6eba0748487d7ddb84d8dd2.jpg',
  },
  createdAt: new Date(), // Добавлено поле с датой создания
  views: 1000, // Пример количества просмотров
  categories: [
    { id: 1, name: 'Природа' },
    { id: 2, name: 'Путешествия' },
  ],
  previewText: 'Это краткое описание поста, которое видно в основном блоке.',
  likes: 50, // Пример количества лайков
  saved: 20, // Пример количества сохранений
  comments: 30, // Пример количества комментариев
  forwards: 10, // Пример количества пересылок
},
{
  id: 1,
  title: 'Заголовок поста 1',
  description: 'Описание поста 1',
  image: 'https://img.freepik.com/free-photo/forest-landscape_71767-127.jpg',
  user: {
    name: 'John Doe',
    avatar: 'path-to-avatar.jpg',
  },
  createdAt: new Date(), // Добавлено поле с датой создания
  views: 1000, // Пример количества просмотров
  categories: [
    { id: 1, name: 'Природа' },
    { id: 2, name: 'Путешествия' },
  ],
  previewText: 'Это краткое описание поста, которое видно в основном блоке.',
  likes: 50, // Пример количества лайков
  saved: 20, // Пример количества сохранений
  comments: 30, // Пример количества комментариев
  forwards: 10, // Пример количества пересылок
},
{
  id: 1,
  title: 'Заголовок поста 1',
  description: 'Описание поста 1',
  image: 'https://img.freepik.com/free-photo/forest-landscape_71767-127.jpg',
  user: {
    name: 'John Doe',
    avatar: 'path-to-avatar.jpg',
  },
  createdAt: new Date(), // Добавлено поле с датой создания
  views: 1000, // Пример количества просмотров
  categories: [
    { id: 1, name: 'Природа' },
    { id: 2, name: 'Путешествия' },
  ],
  previewText: 'Это краткое описание поста, которое видно в основном блоке.',
  likes: 50, // Пример количества лайков
  saved: 20, // Пример количества сохранений
  comments: 30, // Пример количества комментариев
  forwards: 10, // Пример количества пересылок
},
{
  id: 1,
  title: 'Заголовок поста 1',
  description: 'Описание поста 1',
  image: 'https://img.freepik.com/free-photo/forest-landscape_71767-127.jpg',
  user: {
    name: 'John Doe',
    avatar: 'https://s.ekabu.ru/localStorage/post/f8/2f/df/7d/f82fdf7d_resizedScaled_740to986.jpg',
  },
  createdAt: new Date(), // Добавлено поле с датой создания
  views: 1000, // Пример количества просмотров
  categories: [
    { id: 1, name: 'Природа' },
    { id: 2, name: 'Путешествия' },
  ],
  previewText: 'Это краткое описание поста, которое видно в основном блоке.',
  likes: 50, // Пример количества лайков
  saved: 20, // Пример количества сохранений
  comments: 30, // Пример количества комментариев
  forwards: 10, // Пример количества пересылок
},
    // Добавьте другие посты по аналогии
  ]

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
    <NewsCard :newsList="newsData" class="mt-3"/>
    <div class="flex h-screen mt-3">
        
        <!-- <LeftComponent class="flex-grow"/> -->
        <PostCard :postList="postData" class="flex-grow"/>
    
        <RightComponent style="min-width: 300px;"/>
      </div>
    </template>