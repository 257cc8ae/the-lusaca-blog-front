<template>
  <div>
    <h1 v-if="titles != null">
    {{ titles[0] }}
    </h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      titles: null,
    };
  },
  methods: {
    clear() {
      this.msg = "";
    },
  },
  created() {
    fetch("http://localhost:3000")
      .then((response) => {
        return response.json();
      })
      .then((json) => {
        this.titles = json.titles;
      })
      .catch((err) => {
        this.msg = err; // エラー処理
      });
  },
};
</script>