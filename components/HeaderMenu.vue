<template>
  <div class="menu">
    <a href="#hello" :class="{ active: route.hash == '#hello'}">HELLO</a>
    <a href="#groom" :class="{ active: route.hash == '#groom'}">GROOM</a>
    <a href="#bride" :class="{ active: route.hash == '#bride'}">BRIDE</a>
    <a href="#wedding" :class="{ active: route.hash == '#wedding'}">WEDDING</a>
    <a href="#rsvp" :class="{ active: route.hash == '#rsvp'}">RSVP</a>
    <!-- <a href="#seats" :class="{ active: route.hash == '#seats'}">SEATS</a> -->
  </div>
</template>

<script setup lang="ts">
const route = useRoute()
</script>

<style scoped lang="scss">
.menu {
  position: fixed;
  width: 100%;
  z-index: 2;
  padding: 1.5rem 1rem;
  top: 0;
  display: flex;
  justify-content: right;
  gap: 10px;
  font-size: 0.95rem;
  background-color: transparent;
  color: #F7F8F6;
}

a {
  color: #F7F8F6;
  text-decoration: none;
}

a:link {
  color: #F7F8F6;
  text-decoration: none;
}

a:visited {
  color: #F7F8F6;
  text-decoration: none;
}

a:hover {
  color: #F7F8F6;
  background-color: transparent;
  text-decoration: none;
  opacity: 1;
  border-bottom: 2px solid white;
}

a.active {
  color: #F7F8F6;
  background-color: transparent;
  text-decoration: none;
  opacity: 1;
  border-bottom: 2px solid white;
}

@media (max-width: 600px) {
  .menu {
    padding: 1.5rem 1rem;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    flex-direction: column;
    gap: 0.5rem;
    position: relative;
    top: 0px;
    right: 0px;
  }

  a {
    margin-left: 0;
  }
}
</style>