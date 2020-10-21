<template>
  <header>
    <div class="header-main">
      <img src="../assets/logo.svg" width="200px" class="logo" />
      <nav>
        <ul>
          <router-link to="/">
            <li>Home</li>
          </router-link>
          <router-link to="/">
            <li>All Posts</li>
          </router-link>
          <router-link to="/">
            <li>Tags</li>
          </router-link>
          <router-link to="/">
            <li>About</li>
          </router-link>
        </ul>
      </nav>
    </div>
  </header>
</template>
<style>
header {
  width: 100%;
  height: 69px;
  border-bottom: 1px solid #b5bdc4;
  background: #FFF;
}

.header-main {
  width: 100%;
  max-width: 1000px;
  margin-right: auto;
  margin-left: auto;
  height: 69px;
  display: flex;
}

.logo {
  flex: 0 0 auto;
  width: 200px;
  margin: 13.5px 10px;
}

nav {
  flex: 0 0 auto;
}

nav ul {
  margin: 0;
  display: flex;
}

nav ul li {
  list-style: none;
  flex: 0 0 auto;
  margin-left: 10px;
  margin-right: 10px;
  display: inline;
  font-family: "IBM Plex Mono", monospace;
}

nav ul li:hover {
  border-bottom: #b8050b solid 2px;
}

nav ul a {
  text-decoration: none;
  line-height: 69px;
  color: #000;
}
</style>