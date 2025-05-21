<template>
  <div v-show="open" class="modal">
    <div class="content">
      <div class="header">
        Thank you!
      </div>
      <div class="body">
        
      </div class="footer">
    </div>
  </div>
</template>

<script setup lang="ts">
const open = defineModel<boolean>('open', { default: false })
</script>
