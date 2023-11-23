<script>
import listPostsVue from '@/components/posts/list-posts.vue';

export default {
  components:{
    listPostsVue
  },
  data() {
    return {
      userInfo: {},
    };
  }
};
</script>

<template>
    <listPostsVue />
</template>
