<template>
  <div>
    <Teleport to="body">
      <Transition
        name="transition-enabled"
        enter-active-class="enter-active-class"
        leave-active-class="leave-active-class"
      >
        <div
          v-if="open"
          class="modal-container backdrop"
          @click.self.stop="closeModal()"
        >
          <div class="root" >
            <div class="header">
              <h3>Thank you</h3>
            </div>
            <div class="body">
              <div class="qr-code">
                <img src="/assets/qr.jpg" alt="">
              </div>
              <div class="account" @click="handleCopy">
                <span>MN06 0004000 475019521</span>
                <img src="/assets/copy.svg" alt="" class="icon">
              </div>
              <div v-if="copied" class="status">
                <span>Copied account!</span>
              </div>
            </div>
            <div class="footer">
              <span class="button" @click="closeModal">
                Close
              </span>
            </div>
          </div>
        </div>
      </Transition>
    </Teleport>
  </div>
</template>

<script setup lang="ts">
import { useClipboard, useShare } from "@vueuse/core";

const open = defineModel<boolean>('visible', { default: false })
const { copy, copied, } = useClipboard()

const accNum = ref('MN060004000475019521')

const openModal = () => {
  open.value = true
}

const closeModal = () => {
  open.value = false
}

const handleCopy = () => {
  copy(accNum.value)
}

defineExpose({
  openModal,
  closeModal,
})
</script>

<style lang="scss" scoped>
.modal-container {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  height: 100%;
  z-index: 1000;
}
.backdrop {
  background-color: rgba(0, 0, 0, 0.5);
  cursor: default;
}
.root {
  display: flex;
  padding: 0;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  min-width: 200px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
  transition-property: transform, opacity;
  transition: 0.3s ease;
  background-color: rgba(0, 0, 0, 0.75);
  border-radius: 8px;
  border: 2px solid #F7F8F6;
  max-height: 100%;
}

.header {
  font-size: 20px;
  width: 100%;
  text-align: center;
  padding-top: 30px;
  padding-bottom: 30px;
  color: #F7F8F6;
}

.qr-code {
  width: 100%;
  max-width: 385px;
  padding-left: 30px;
  padding-right: 30px;
  padding-bottom: 15px;
  img {
    width: 100%;
    border-radius: 7px;
  }
}

.body {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.account {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 5px;
  background-color: #333335;
  padding-left: 20px;
  padding-right: 10px;
  padding-top: 10px;
  padding-bottom: 10px;
  border-radius: 20px;
  .icon {
    height: 20px;
    width: 20px;
  }
}

.footer {
  padding-top: 30px;
  padding-bottom: 30px;
  span {
    font-size: 15px;
    font-weight: bold;
  }
}

.status {
  padding-top: 10px;
}

.enter-active-class,
.leave-active-class {
  transition: 0.3s ease;
}
.transition-enabled-enter-from .root,
.transition-enabled-leave-to .root {
  transform: scale(0.3);
  opacity: 0;
}
</style>
