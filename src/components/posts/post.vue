<script>
import axios from "axios";

export default {
  props: {
    item: {
      required: true,
    },
  },
  data() {
    return {
      responseData: null,
    };
  },
  mounted() {},
};
</script>

<template>
  <div class="post">
    <h1>{{ item.title }}</h1>
    <div class="post-body">
      {{ item.body }}
    </div>
  </div>
</template>

<style>
h1,
p {
  margin: 0;
}

.post {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(223, 5, 5, 0.1);
  margin: 20px;
}

.post-title {
  font-size: 1.5rem;
  font-weight: bold;
}

.post-body {
  font-size:32px;
  margin-top: 10px;
}
</style>
