<template>
  <div class="popup popup-wht welcome" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <img src="..\..\assets\Image443.png" alt="" />
    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">
          How many opportunities do you want for your business <br />
          Jeremy Anthony!
        </h2>

        <p class="popup-text">
          The more networking you do, the more opportunities will come your way!
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
  name: "WelcomeOpportunity",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
</style>