<template>
  <div class="home">
    <HomeShowPosts/>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeShowPosts from '@/components/HomeShowPosts.vue'

export default {
  name: 'Home',
  components: {
    HomeShowPosts
  }
}
</script>
