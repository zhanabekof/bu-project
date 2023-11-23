<template>
  <div id="app">
    <UserForm @form-submitted="updateUserInfo" />
    <UserInfo :user="userInfo" />
  </div>
</template>

<script>
import UserForm from "@/components/UserForm.vue";
import UserInfo from "@/components/UserInfo.vue";

export default {
  components: {
    UserForm,
    UserInfo,
  },
  data() {
    return {
      userInfo: {},
    };
  },
  methods: {
    updateUserInfo(user) {
      console.log(user);
      this.userInfo = user;
    },
  },
};
</script>

<style>
/* Ваши глобальные стили */
body {
  font-family: "Arial", sans-serif;
  background-color: #f4f4f4;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

#app {
  text-align: center;
}

.user-form {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
}

.user-info {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
</style>
