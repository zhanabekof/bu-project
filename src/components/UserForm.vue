<template>
    <div class="user-form">
      <input v-model="user.name" id="name" type="text" placeholder="Имя" />
      <input v-model="user.phone" id="phone" type="text" placeholder="Телефон" />
      <input v-model="user.age" id="age" type="number" placeholder="Возраст" />
      <input v-model="user.birthday" placeholder="Дата рождения" id="birthday" type="text" />
      <input v-model="user.children" placeholder="Сколько детей" id="name" type="text" />
      <!-- Добавьте остальные поля формы -->
        <br />
      <button class="button-primary" @click="submitForm">Отправить</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        user: {
          name: "",
          phone:"",
          age:"",
          birthday:"",
          children:""
        },
      };
    },
    methods: {
      submitForm() {
        this.$emit("form-submitted", { ...this.user });
        this.user = {}; // Очистка полей формы
      },
    },
  };
  </script>
  
  <style scoped>
    input{
        padding: 10px;
        margin: 10px;
    }
    .button-primary{
        background-color: blue;
        color: white;
        margin: 10px;
        padding: 10px 30px;
    }
  </style>
  