<template>
  <div class="popup" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>

    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">
          there's someone waiting to network right now!
        </h2>

        <span class="desk-only">
          <p class="popup-text">
            Don't delay! Click before 2 mins past the hour to be included
          </p>
          <button @click="hidePopup" class="popup-btn">
            join this Meeow now
          </button>
          <a href="" @click="hidePopup">
            Thanks... I'm not Meeowing this hour
          </a>
        </span>

        <span class="mob-only">
          <p class="popup-text">
            Jump onto your computer or tablet to join this Meeow!
          </p>
          <button @click="hidePopup" id="close-mob-btn">close</button>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SomeoneClicked",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
@media only screen and (max-width: 480px) {
  .popup-title {
    width: 260px;
  }
}
</style>