<template>
    <div class="user-info">
      <h2>Иинформация о пользователе</h2>
        <p>Имя: {{ user.name }}</p>
        <p>Телефон: {{ user.phone }}</p>
        <p>Возраст: {{ user.age }}</p>
        <p>Дата рождения: {{ user.birthday }}</p>
        <p>Количество детей: {{ user.children }}</p>
        
        <!-- Отображение остальных полей -->

    </div>
  </template>
  
  <script>
  export default {
    props: {
      user: {
        type: Object,
        default: () => ({}),
      },
    },
  };
  </script>
  
  <style scoped>
    p{
        margin: 20px;
    }
  </style>
  