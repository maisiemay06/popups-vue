<template>
  <div class="popup popup-wht welcome" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <img src="..\..\assets\Image436.png" alt="" />
    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">
          Welcome back <br />
          Benedict!
        </h2>

        <p class="popup-text">
          It's great to see you back, we missed you ;&#41;
        </p>
        <p class="popup-text">
          The Meeow community is waiting to see you, so get yourself booked into
          lots of lovely Meeows over the next couple of weeks.
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
  name: "WelcomeBack",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
</style>