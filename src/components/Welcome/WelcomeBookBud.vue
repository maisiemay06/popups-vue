<template>
  <div class="popup popup-wht welcome" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <img src="..\..\assets\Image440.png" alt="" />
    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">
          Don't forget the <br />
          Book Buddies <br />
          Jeremy Anthony!
        </h2>

        <p class="popup-text">
          You can see when other Meeowists have booked to network by looking for
          the 'Book Buddies' on the calendar.
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
  name: "WelcomeBookBud",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
</style>