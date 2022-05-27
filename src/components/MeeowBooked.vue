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
          We've sent you a confirmation email to prove it.
        </p>
        <p class="popup-text footer">
          careful... entry to every Meeow closes at 3 mins past the hour
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

#close-btn {
  top: -75px;
}

.popup-subtitle {
  margin-top: -20px;
}

.footer {
  margin-top: 90px;
  margin-bottom: -30px;
}

@media only screen and (max-width: 480px) {
  .footer {
    margin-top: 40px;
    margin-bottom: 0;
  }
}
</style>