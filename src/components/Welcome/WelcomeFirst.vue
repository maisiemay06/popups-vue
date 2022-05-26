<template>
  <div class="popup popup-wht welcome" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <img src="..\..\assets\Image438.png" alt="" class="smaller-img" />
    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">
          Welcome to the hottest networking in the world <br />
          Carolina Julia!
        </h2>

        <p class="popup-text">
          Don't forget to book your first Meeows right now to make sure you get
          off to a flying networking start!
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
  name: "WelcomeFirst",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
.smaller-img {
  height: 152px;
}
@media only screen and (max-width: 480px) {
  .smaller-img {
    height: 90px;
    margin-top: 40px;
  }
}
</style>