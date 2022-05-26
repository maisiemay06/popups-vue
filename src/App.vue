<template>
  <!-- Background image of calendar only for show -->
  <img src="./assets/background.png" alt="" id="background" />

  <div class="welcome-buttons">
    <button @click="() => showPopup('WelcomeSeasonal')">
      Welcome Seasonal
    </button>
    <button @click="() => showPopup('WelcomeBack')">Welcome Back</button>
    <button @click="() => showPopup('WelcomeBack2')">Welcome Back 2</button>
    <button @click="() => showPopup('WelcomeFirst')">Welcome First Time</button>
    <button @click="() => showPopup('WelcomeTellFriend')">
      Welcome Tell Friend
    </button>
    <button @click="() => showPopup('WelcomeFeedback')">
      Welcome Feedback
    </button>
    <button @click="() => showPopup('Welcome3Week')">Welcome 3 a Week</button>
    <button @click="() => showPopup('WelcomeBookBud')">
      Welcome Book Buddies
    </button>
    <button @click="() => showPopup('WelcomeAmbassador')">
      Welcome Ambassador
    </button>
  </div>

  <welcome-seasonal
    v-if="popupOpen && popupContent === 'WelcomeSeasonal'"
    :hidePopup="hidePopup"
  ></welcome-seasonal>
  <welcome-back
    v-if="popupOpen && popupContent === 'WelcomeBack'"
    :hidePopup="hidePopup"
  ></welcome-back>
  <welcome-back-2
    v-if="popupOpen && popupContent === 'WelcomeBack2'"
    :hidePopup="hidePopup"
  ></welcome-back-2>
  <welcome-first
    v-if="popupOpen && popupContent === 'WelcomeFirst'"
    :hidePopup="hidePopup"
  ></welcome-first>
  <welcome-tell-friend
    v-if="popupOpen && popupContent === 'WelcomeTellFriend'"
    :hidePopup="hidePopup"
  ></welcome-tell-friend>
  <welcome-feedback
    v-if="popupOpen && popupContent === 'WelcomeFeedback'"
    :hidePopup="hidePopup"
  ></welcome-feedback>
  <welcome-3-week
    v-if="popupOpen && popupContent === 'Welcome3Week'"
    :hidePopup="hidePopup"
  ></welcome-3-week>
  <welcome-book-bud
    v-if="popupOpen && popupContent === 'WelcomeBookBud'"
    :hidePopup="hidePopup"
  ></welcome-book-bud>
  <welcome-ambassador
    v-if="popupOpen && popupContent === 'WelcomeAmbassador'"
    :hidePopup="hidePopup"
  ></welcome-ambassador>

  <div class="demo-buttons">
    <button @click="() => showPopup('MeeowBooked')">Booked a Meeow</button>
    <button @click="() => showPopup('NextMeeow')">Next Meeow Starting</button>
    <button @click="() => showPopup('BookedStarting')">
      Booked Meeow Starting
    </button>
    <button @click="() => showPopup('SomeoneClicked')">
      Someone Else Clicked
    </button>
    <button @click="() => showPopup('NoOneThere')">No One There</button>
    <button @click="() => showPopup('TellFriend')">Tell a Friend</button>
    <button @click="() => showPopup('JustJoined')">
      I've Just Joined Meeow
    </button>
    <button @click="() => showPopup('JustBooked')">
      I've Just Booked a Meeow
    </button>
  </div>

  <meeow-booked
    v-if="popupOpen && popupContent === 'MeeowBooked'"
    :hidePopup="hidePopup"
  ></meeow-booked>
  <next-meeow
    v-if="popupOpen && popupContent === 'NextMeeow'"
    :hidePopup="hidePopup"
  ></next-meeow>
  <booked-starting
    v-if="popupOpen && popupContent === 'BookedStarting'"
    :hidePopup="hidePopup"
  ></booked-starting>
  <someone-clicked
    v-if="popupOpen && popupContent === 'SomeoneClicked'"
    :hidePopup="hidePopup"
  ></someone-clicked>
  <no-one-there
    v-if="popupOpen && popupContent === 'NoOneThere'"
    :hidePopup="hidePopup"
  ></no-one-there>
  <tell-friend
    v-if="popupOpen && popupContent === 'TellFriend'"
    :hidePopup="hidePopup"
  ></tell-friend>
  <just-joined
    v-if="popupOpen && popupContent === 'JustJoined'"
    :hidePopup="hidePopup"
  ></just-joined>
  <just-booked
    v-if="popupOpen && popupContent === 'JustBooked'"
    :hidePopup="hidePopup"
  ></just-booked>
</template>

<script>
import "./style.css";
// import PopupTemplate from "./components/PopupTemplate.vue";
import MeeowBooked from "./components/MeeowBooked.vue";
import NextMeeow from "./components/NextMeeow.vue";
import BookedStarting from "./components/BookedStarting.vue";
import SomeoneClicked from "./components/SomeoneClicked.vue";
import NoOneThere from "./components/NoOneThere.vue";
import TellFriend from "./components/TellFriend.vue";
import JustJoined from "./components/JustJoined.vue";
import JustBooked from "./components/JustBooked.vue";

import WelcomeSeasonal from "./components/Welcome/WelcomeSeasonal";
import WelcomeBack from "./components/Welcome/WelcomeBack";
import WelcomeBack2 from "./components/Welcome/WelcomeBack2";
import WelcomeFirst from "./components/Welcome/WelcomeFirst";
import WelcomeTellFriend from "./components/Welcome/WelcomeTellFriend";
import WelcomeFeedback from "./components/Welcome/WelcomeFeedback";
import Welcome3Week from "./components/Welcome/Welcome3Week";
import WelcomeBookBud from "./components/Welcome/WelcomeBookBud";
import WelcomeAmbassador from "./components/Welcome/WelcomeAmbassador";

export default {
  name: "App",
  components: {
    // PopupTemplate,
    MeeowBooked,
    NextMeeow,
    BookedStarting,
    SomeoneClicked,
    NoOneThere,
    TellFriend,
    JustJoined,
    JustBooked,

    WelcomeSeasonal,
    WelcomeBack,
    WelcomeBack2,
    WelcomeFirst,
    WelcomeTellFriend,
    WelcomeFeedback,
    Welcome3Week,
    WelcomeBookBud,
    WelcomeAmbassador,
  },
  data() {
    return {
      popupOpen: false,
      popupContent: "",
      popupColor: "",
    };
  },
  methods: {
    showPopup(content, color) {
      this.popupOpen = true;
      this.popupContent = content;
      this.popupColor = color;
    },
    hidePopup() {
      this.popupOpen = false;
    },
  },
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
#background {
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
}
.welcome-buttons {
  position: fixed;
  bottom: 20px;
  right: 220px;
  display: block;
}
.demo-buttons {
  position: fixed;
  bottom: 20px;
  right: 20px;
}
button {
  font-family: sofia-pro, sans-serif;
  background-color: var(--accent-blue);
  border: none;
  border-radius: 4px;
  padding: 5px;
  width: 180px;
  margin-bottom: 10px;
  color: #fff;
  display: block;
}
</style>
