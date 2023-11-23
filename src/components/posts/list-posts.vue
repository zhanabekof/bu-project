<script>
import axios from 'axios';
export default {
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
      axios.get('https://jsonplaceholder.typicode.com/posts')
        .then(response => {
          this.responseData = response.data;
        })
        .catch(error => {
          console.error('Error fetching data:', error);
        });
    },
  },
};

</script>

<template>
    <div v-for="item in responseData">
        <p>{{ item.body }}</p>
    </div>
</template>
