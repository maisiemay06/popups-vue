<template>
  <div class="popup popup-wht welcome" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <img src="..\..\assets\Image439.png" alt="" />
    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">
          Getting your 3 a week <br />
          Jeremy Anthony?
        </h2>

        <p class="popup-text">
          The best way to keep the opportunities flowing for your business is to
          make sure you have at least 3 networking sessions a week.
        </p>
        <button @click="hidePopup" class="popup-btn">
          let's book some Meeows
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Welcome3Week",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
</style>