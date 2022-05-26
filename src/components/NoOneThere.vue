<template>
  <div class="popup popup-wht" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>

    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">sorry</h2>
        <img src="..\assets\sorry-emoji.png" alt="sorry emoji" class="emoji" />

        <p class="popup-text">
          There's no one else to Meeow with at the moment.
        </p>
        <p class="popup-text">
          Choose a busier time slot by looking for the Book Buddies, or even
          book a slot to attract people to network when you want to.
        </p>
        <div class="book-buddies">
          <img
            src="..\assets\blue-user-icon.png"
            alt="blue user icon"
            class="user-icon"
          />
          <img
            src="..\assets\orange-user-icon.png"
            alt="orange user icon"
            class="user-icon"
          />
        </div>
        <button @click="hidePopup" class="popup-btn">book more Meeows</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NoOneThere",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
.popup-title {
  display: inline;
  margin-right: 20px;
}
.emoji {
  height: 36px;
}
.popup-text {
  max-width: 500px;
}
.user-icon {
  display: inline-block;
  height: 48px;
  margin: 10px 8px 15px 8px;
}
</style>