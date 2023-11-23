<script>
import axios from "axios";
import Post from '@/components/posts/post.vue';;

export default {
  components: {
    Post,
  },
  data() {
    return {
      responseData: null,
    };
  },
  mounted() {
    this.getData();
  },
  methods: {
    getData() {
      // Replace the URL with the actual API endpoint
      axios
        .get("https://jsonplaceholder.typicode.com/posts")
        .then((response) => {
          this.responseData = response.data;
        })
        .catch((error) => {
          console.error("Error fetching data:", error);
        });
    },
  },
};
</script>

<template>
  <div v-for="item in responseData">
    <Post :item="item"></Post>
  </div>
</template>

