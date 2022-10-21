<template>
  <div class="introMain">
    <video :width="screenwidth" :height="screenheight - 150" autoplay muted>
      <source
        src="https://res.cloudinary.com/dnlxvy81c/video/upload/v1665571708/Ijas_g8kbzm.mp4"
        type="video/mp4"
      />
    </video>
    <!-- <img
      src="https://res.cloudinary.com/dnlxvy81c/image/upload/v1665051909/WhatsApp_Image_2022-09-30_at_3.15.47_PM_ky1kqm.jpg"
      alt="ijas.jpg"
      class="myPic"
    /> -->
  </div>
</template>

<script setup>
let screenwidth = screen.width;
let screenheight = screen.height;
</script>

<style scoped>
.introMain {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
