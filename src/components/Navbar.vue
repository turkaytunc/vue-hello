<template>
  <nav class="nav-bar">
    <a href="http://www.google.com" target="blank">Google</a>
    <a href="http://www.eksisozluk.com" target="blank">Eksi</a>
    <a href="http://www.reddit.com" target="blank">Reddit</a>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
};
</script>

<style>
.nav-bar {
  background-color: #333;
  color: white;
  width: 100%;
}
a {
  color: white;
  text-decoration: none;
}
a:not(:first-child) {
  padding-left: 1rem;
}
</style>
