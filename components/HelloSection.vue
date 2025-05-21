<template>
  <div class="page" id="hello">
    <div class="background">
    </div>
    <div class="section">
      <div class="left">
        <h2>- We are <br> getting married</h2>
      </div>
      <div class="mid">
        <img src="/assets/hello.jpg" alt="Hello">
      </div>
      <div class="end">
        Hey! Welcome to our wedding website! <br> Here's where you'll find all the fun details about our big day and a little bit about us. Check it out and get ready to celebrate!
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
  background-image: url("/assets/hello_background.png");
  background-position: center;
  background-size: contain;
}

.left {
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

@media (max-width: 600px) {
  .page {
    height: 100%;
    width: 100vw;
  }
  .section {
    flex-direction: column;
  }

  .left {
    align-self: flex-end;
    h2 {
      font-size: 2rem;
    }
  }

  .mid {
    align-self: center;
    img {
      width: 400px;
    }
  }

  .end {
    align-self: center;
  }
}
</style>