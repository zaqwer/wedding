<template>
  <div class="footer">
    <div class="title">
      <p>Ebi & Bugi</p>
    </div>
    <div class="action" @click="handleClick">
      <p>If you wanted</p>
    </div>
  </div>
</template>

<script setup lang="ts">
const handleClick = () => {
  console.log('showModal')
}
</script>

<style scoped lang="scss">
.footer {
  position: fixed;
  bottom: 0;
  font-size: 1rem;
  width: 100%;
  display: flex;
  justify-content: space-between;
  p {
    margin: 0;
    padding: 0 30px 20px 30px;
  }
  .title {
    font-weight: bold;
  }

  .action {
    cursor: pointer;
  }
}
</style>