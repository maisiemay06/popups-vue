<template>
  <div class="popup popup-wht welcome" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <img src="..\..\assets\Image441.png" alt="" />
    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">
          Hey! how's it going <br />
          Jeremy Anthony?
        </h2>

        <p class="popup-text">
          We love regular feedback on how Meeow is helping you drive your
          business forward. Feel free to click on the speech bubble in the
          bottom right hand corner and tell us what you think.
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
  name: "WelcomeFeedback",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
</style>