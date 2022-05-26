<template>
  <div class="popup popup-wht welcome" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <img src="..\..\assets\Image437.png" alt="" />
    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">
          You can't stay away <br />
          Anthony!
        </h2>

        <p class="popup-text">
          It's great to see such a dedicated Meeowist coming back time and again
          to network with the world... brings a tear to our collective eye.
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
  name: "WelcomeBack2",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
</style>