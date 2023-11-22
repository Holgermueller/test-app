<template>
  <div id="Experience">
    <div class="image">
      <div class="caption">
        <span class="border">PORTFOLIO</span>
      </div>
    </div>

    <div class="experience-container"></div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.image {
  /* image by Pixabay via Pexels */
  background-image: url("../images/portfoliobanner.png");
  background-size: cover;
  height: 500px;
  width: 100%;
}
.caption {
  width: 100%;
  position: relative;
  left: 0;
  top: 50%;
  text-align: center;
  color: black;
}
.caption span.border {
  background-color: #31708e;
  color: white;
  width: fit-content;
  font-size: 25px;
  padding: 18px;
  letter-spacing: 10px;
}
</style>
