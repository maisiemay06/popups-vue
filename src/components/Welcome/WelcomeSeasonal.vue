<template>
  <div class="popup popup-wht welcome" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <img src="..\..\assets\Image434.png" alt="" />
    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">
          Happy Christmas <br />
          Antonella Jane <br />
          from everyone at Meeow!
        </h2>

        <p class="popup-text">
          How about a little Christmas networking to get you in the festive
          spirit?
        </p>
        <p class="popup-text">Click on the calendar slots to book.</p>
        <button @click="hidePopup" class="popup-btn">
          let's book some Meeows
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "WelcomeSeasonal",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
</style>