<template>
  <div>
    <div v-if="posts === null">
      <h2>Now Loading</h2>
    </div>
    <div v-else-if="posts === 'Error'">
      <h2>There was a problem loading.</h2>
    </div>
    <div v-else>
      <div v-for="post in posts" :key="post.title">
        <div v-if="post.thumbnail != ''">
          <img v-bind:src="post.thumbnail" loading="lazy" alt="Thumbnail Image" class="thumbnail">
        </div>
        <h2 class="post-title">{{ post.title }}</h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: null,
    };
  },
  created() {
    fetch("http://localhost:3000")
      .then((response) => {
        return response.json();
      })
      .then((json) => {
        this.posts = json;
      })
      .catch((err) => {
        this.posts = "Error";
        console.log(err);
      });
  },
};
</script>

<style>
.thumbnail {
  width: 100%;
}
.post-title {
  font-size: 25px;
  padding: 20px;
  margin: 0;
}
</style>