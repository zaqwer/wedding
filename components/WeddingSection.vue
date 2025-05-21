<template>
  <div class="page" id="wedding">
    <div class="background">
    </div>
    <div class="section">
      <div class="left">
        <h2>- Save the date</h2>
      </div>
      <div class="mid">
        <img src="/assets/wedding.jpg" alt="Hello">
      </div>
      <div class="end">
        <div>
          <span>
            Date
          </span>
          <span>
            May 29
          </span>
        </div>
        <div>
          <span>
            Time
          </span>
          <span>
            18:00
          </span>
        </div>
        <div>
          <span>
            Location
          </span>
          <span>
            One Event Hall
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
.page {
  background: #333335;
  background: linear-gradient(0deg,rgba(51, 51, 53, 1) 0%, rgba(34, 34, 34, 1) 50%, rgba(23, 23, 25, 1) 100%);
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: left;
  height: 100vh;
  width: 100vw;
  padding: 2rem;
  position: relative;
  scroll-snap-align: start;
}

.section {
  width: 100%;
  max-width: 1200px;
  display: flex;
  justify-content: space-between;
  gap: 20px;
  background-image: url("/assets/wedding_background.png");
  background-position: center;
  background-size: contain;
}

.left{
  align-self: flex-start;
  width: 200px;
  h2 {
    font-size: 2.5rem;
    font-weight: bold;
    line-height: 1.2;
  }
}

.mid {
  align-self: flex-center;
  img {
    width: 500px;
    max-width: 100%;
    border-radius: 10px;
  }
}

.end {
  align-self: flex-end;
  max-width: 300px;
  font-size: 0.95rem;
  line-height: 1.6;
}
</style>