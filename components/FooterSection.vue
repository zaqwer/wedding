<template>
  <div class="footer">
    <div class="title">
      <p>Ebi & Bugi</p>
    </div>
    <div class="action" @click="handleClick">
      <p>Wanna send wedding gift?</p>
    </div>
  </div>
  <GiftModal ref="modal"/>
</template>

<script setup lang="ts">
const modal = useTemplateRef('modal')
const handleClick = () => {
  modal.value.openModal()
}
</script>

<style scoped lang="scss">
.footer {
  position: fixed;
  bottom: 0;
  font-size: 1rem;
  width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  mix-blend-mode: difference;

  p {
    margin: 0;
    padding: 0 30px 20px 30px;
  }
  .title {
    font-weight: bold;
  }

  .action {
    cursor: pointer;
    text-align: center;
    max-width: 200px;
  }
}
</style>