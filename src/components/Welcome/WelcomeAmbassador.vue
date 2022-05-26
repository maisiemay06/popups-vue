<template>
  <div class="popup popup-wht welcome" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <div class="images">
      <img src="..\..\assets\ambassador.png" alt="" />
      <img src="..\..\assets\superAmbassador.png" alt="" />
    </div>

    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title smaller-title">
          Apply to be an Ambassador and earn shares in Meeow <br />
          Jeremy Anthony!
        </h2>

        <p class="popup-text">
          Would you like to be a shareholder in the fastest growing, global
          networking startup in the world?
        </p>
        <button @click="hidePopup" class="popup-btn">find out more</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "WelcomeAmbassador",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
.welcome {
  margin-top: 18vh;
}
img {
  margin: 100px 5px 20px 5px;
  height: 160px;
}
.popup-title {
  width: 90%;
}
.smaller-title {
  width: 75%;
  margin-inline: auto;
}

@media only screen and (max-width: 480px) {
  img {
    height: 100px;
  }
  .smaller-title {
    width: 100%;
  }
}
</style>