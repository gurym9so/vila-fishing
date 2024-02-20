<template>
  <div class="header">
    <div class="header_wrapper wrapper">
      <a class="logo" href="/">vilaFishing</a>
      <ul class="navbar-list">
        <li v-for="link in links" :key="link.alias">
          <a class="list-item" :href="link.url">{{ link.title }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import { links } from "@/_config.js";
export default {
  data() {
    return {
      links: links,
    };
  },
};
</script>

<style>
.wrapper {
  width: 80%;
}
.header {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}
.header_wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 40px 0 40px 0;
}
.logo {
  font-size: 22px;
  text-decoration: none;
  color: black;
}
.navbar-list {
  display: flex;
  flex-direction: row;
  gap: 30px;
  font-size: 22px;
  list-style-type: none;
}
.list-item {
  text-decoration: none;
  color: black;
}
</style>
