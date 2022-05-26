<template>
  <div class="popup popup-wht welcome" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>
    <img src="..\..\assets\Image442.png" alt="" />
    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">
          Tell a friend about Meeow <br />
          Jeremy Anthony?
        </h2>

        <p class="popup-text">
          Don't keep Meeow a secret... the best way of making sure there's
          always someone new and interesting for you to meet is by spreading the
          word.
        </p>
        <button @click="handleClick" class="popup-btn">
          tell a friend about Meeow
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "WelcomeTellFriend",
  props: {
    hidePopup: Function,
    showPopup: Function,
  },
  methods: {
    handleClick() {
      this.showPopup("TellFriend");
    },
  },
};
</script>

<style scoped>
</style>