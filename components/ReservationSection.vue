<template>
  <div class="page" id="rsvp">
    <div class="background">
    </div>
    <div class="section">
      <div>
        <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSf8RAYSfIHdRf7qWZ-2Bw2syDLJli71FJarJhunuXbNjz0s7A/viewform?embedded=true" width="390" height="950" frameborder="0" marginheight="0" marginwidth="0" class="rsvp">Loading…</iframe>
      </div>
    </div>
  </div>
</template>

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
  height: 100%;
  width: 100vw;
  padding: 2rem;
  position: relative;
  scroll-snap-stop: unset;
}

.section {
  width: 100%;
  max-width: 1200px;
  display: flex;
  justify-content: center;
  gap: 20px;
  background-image: url("/assets/rsvp_background.png");
  background-position: center;
  background-size: contain;
}

@media (max-width: 600px) {
  .page {
    height: 100%;
    width: 100vw;
  }
}
</style>