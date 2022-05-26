<template>
  <transition name="fade" appear>
    <div class="popup-overlay" @click="hidePopup"></div>
  </transition>

  <transition name="pop" appear>
    <div class="popup popup-wht" role="dialog">
      <p id="close-btn" @click="hidePopup">&times;</p>

      <div class="popup-container">
        <div class="popup-content">
          <h2 class="popup-title">the next Meeow is about to start</h2>

          <span class="desk-only">
            <p class="popup-text">
              Click before 2 mins past the hour to be included
            </p>
            <button @click="hidePopup" class="popup-btn">
              join this Meeow now
            </button>
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
  </transition>
</template>

<script>
export default {
  name: "NextMeeow",
  props: {
    hidePopup: Function,
  },
};
</script>

<style scoped>
</style>