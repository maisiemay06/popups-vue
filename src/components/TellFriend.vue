<template>
  <div class="popup popup-wht invite-friends" role="dialog">
    <p id="close-btn" @click="hidePopup">&times;</p>

    <div class="popup-container">
      <div class="popup-content">
        <h2 class="popup-title">tell your friends about Meeow</h2>

        <p class="popup-text">
          Every new member of Meeow makes the community bigger and better for
          you and everyone around the world. Invite your friends to join the
          Meeow community for free.
        </p>
        <p class="popup-small">
          Type your friends' email addresses into the slots below to invite them
          to join Meeow
        </p>

        <div class="invite-fields">
          <input type="email" placeholder="Friend 1" v-model="enteredEmail1" />
          <input type="email" placeholder="Friend 2" v-model="enteredEmail2" />
          <input type="email" placeholder="Friend 3" v-model="enteredEmail3" />
          <input type="email" placeholder="Friend 4" v-model="enteredEmail4" />
          <input type="email" placeholder="Friend 5" v-model="enteredEmail5" />
        </div>

        <button
          v-if="!invitesSent"
          id="send-invite-btn"
          class="popup-btn invite-btn"
          :disabled="buttonDisabled"
          @click="handleSubmit"
        >
          send your invitations now
        </button>
        <button
          v-else
          id="sent-invite-btn"
          class="popup-btn invite-btn"
          disabled
        >
          invitations sent! thank you
        </button>
      </div>
      <a href="" @lick="hidePopup"> Don't show me this again </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "NextMeeow",
  props: {
    hidePopup: Function,
  },

  data() {
    return {
      invitesSent: false,
      enteredEmail1: "",
      enteredEmail2: "",
      enteredEmail3: "",
      enteredEmail4: "",
      enteredEmail5: "",
      buttonDisabled: true,
    };
  },
  watch: {
    enteredEmail1() {
      this.checkEmail(this.enteredEmail1);
    },
    enteredEmail2() {
      this.checkEmail(this.enteredEmail2);
    },
    enteredEmail3() {
      this.checkEmail(this.enteredEmail3);
    },
    enteredEmail4() {
      this.checkEmail(this.enteredEmail4);
    },
    enteredEmail5() {
      this.checkEmail(this.enteredEmail5);
    },
  },
  methods: {
    validateEmail(email) {
      const regex =
        /^([a-zA-Z0-9_.+-])+@(([a-zA-Z0-9-])+.)+([a-zA-Z0-9]{2,6})+$/;
      return regex.test(email);
    },
    checkEmail(email) {
      if (this.validateEmail(email)) {
        this.buttonDisabled = false;
        console.log("enabled");
      } else {
        this.buttonDisabled = true;
        console.log("disabled");
      }
    },
    handleSubmit() {
      this.invitesSent = true;
    },
  },
};
</script>

<style scoped>
.invite-friends {
  width: 656px;
  height: 90vh;
  max-height: 900px;
  margin-top: 6vh;
  box-sizing: border-box;
  padding-bottom: 30px;
}

.popup-small {
  color: #757a7f;
  margin-top: 15px;
  margin-bottom: 20px;
  font-size: 0.875rem;
}

input {
  display: block;
  width: 96%;
  height: 50px;
  margin-bottom: 10px;
  background-color: #f7f7f7;
  outline: none;
  border: none;
  padding-left: 20px;
  color: #000;
}
input::placeholder {
  color: #9f9f9f;
}

.invite-btn {
  width: 302px;
  height: 50px;
  margin-top: 40px;
  margin-bottom: 0;
}
#send-invite-btn:disabled {
  background-color: #c9c9c9;
}
#sent-invite-btn {
  background-color: var(--accent-blue);
}
#sent-invite-btn:hover {
  background-color: #04cccc;
}
a {
  margin-top: 0;
  padding-bottom: 20px;
}

@media only screen and (max-width: 480px) {
  .invite-friends {
    width: 85vw;
  }
  .popup-container {
    padding-block: 20px;
  }
  .invite-fields {
    padding: 0 10px;
    width: 90%;
  }
  input {
    height: 40px;
  }
}
</style>