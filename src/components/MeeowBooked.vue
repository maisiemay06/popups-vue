<template>
  <div class="popup" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <div class="popup-container">
      <div class="popup-content">
        <img
          src="..\assets\clapping-emoji.png"
          alt="clapping emoji"
          class="emoji"
        />
        <h2 class="popup-title">you booked a Meeow!</h2>
        <p class="popup-subtitle">
          come back to the calendar at the time of your booking
        </p>
        <p class="popup-text">
          &#40;entry to every Meeow closes at 3 mins past the hour&#41;
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MeeowBooked",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
.popup .emoji {
  height: 55px;
  margin-bottom: 10px;
}
</style>