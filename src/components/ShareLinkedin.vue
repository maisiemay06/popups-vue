<template>
  <div class="popup share-linkedin" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>

    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">help us make Meeow amazing, for you!</h2>

        <p class="popup-text">
          The more people join the Meeow community, the more new connections
          everyone can make.
        </p>
        <p class="popup-text desk-only">
          Click below to place an automated post just like the example on the
          right onto your Linkedin feed.
        </p>
        <p class="popup-text mob-only">
          Click below to place a post onto your Linkedin feed.
        </p>
        <p class="popup-text">
          Don't forget to tag anyone you think would benefit from Meeow
          membership.
        </p>
        <button @click="hidePopup" class="popup-btn">
          post to Linked in now
        </button>
        <a href="">Don't show me this again</a>
      </div>

      <div class="image-container">
        <img :src="require(`../assets/${image}`)" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ShareLinkedin",
  props: {
    hidePopup: Function,
    image: String,
  },
};
</script>

<style scoped>
.share-linkedin {
  width: 80vw;
  max-width: 1330px;
  height: 75vh;
  max-height: 638px;
  margin-top: 12vh;
  padding: 0;
}
.share-linkedin #close-btn {
  color: var(--main-blue);
  right: 13px;
  top: -75px;
}

.popup-container {
  display: grid;
  grid-template-columns: repeat(2, 50%);
}
.popup-content {
  text-align: left;
  padding-left: 60px;
  padding-right: 20px;
  margin-top: 0;
  display: flex;
  flex-wrap: wrap;
  align-content: space-between;
  justify-content: flex-start;
}
.popup-title {
  width: 90%;
}
button {
  background-color: #fff;
  margin: 10px 0;
  height: 45px;
}
button:hover {
  background-color: #f7f7f7;
}
a {
  display: block;
  width: 100%;
}
.image-container {
  background-color: #fff;
  height: 100%;
  padding-bottom: 25px;
  padding-top: 25px;
  display: flex;
  justify-content: center;
  align-items: center;
}
img {
  height: 80%;
}

@media only screen and (max-width: 480px) {
  .share-linkedin #close-btn {
    color: #fff;
  }
  .popup-container {
    display: block;
  }
  .popup-content {
    text-align: center;
    padding: 30px;
  }
  .popup-title {
    width: 100%;
  }
  button {
    background-color: var(--accent-blue);
    margin: auto;
    margin-top: 20px;
  }
  a {
    padding-bottom: 20px;
  }
  img {
    margin-top: -230px;
  }
}
</style>