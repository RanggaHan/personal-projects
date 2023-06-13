<!-- Landing Page -->
<template>
  <div class="landing-page">
    <div class="landing-page__content">
      <h1>Welcome!</h1>
      <h1>{{ message }}</h1>
      <div class="yes-no-buttons">
        <button class="landing-page__button" @click="chooseOption('yes')">
          Yes
        </button>
        <button class="landing-page__button" @click="chooseOption('no')">
          No
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LandingPage",
  data() {
    return {
      message: "Are you Kyra by any chance...",
    };
  },
  methods: {
    chooseOption(option) {
      if (option === "yes") {
        this.message = "Yes, you found me!";
      } else if (option === "no") {
        this.message = "Oh, that's too bad...";
      }
    },
  },
};
</script>

<style scoped>
.landing-page {
  /* background-color: #42b983; */
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
}
.landing-page__content {
  background-color: #fff;
  height: 50vh;
  width: 50vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.landing-page__content h1 {
  color: #42b983;
  font-size: 2rem;
  margin: 0;
  animation: landing-page-h1 5000ms ease 0s 1 normal forwards;
  color: rgba(0, 0, 0, 0.8);
}
.yes-no-buttons {
  margin-top: 12px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.landing-page__button {
  background-color: #000000;
  border: solid 1px #000000;
  color: #fff;
  padding: 10px 20px;
  margin: 10px;
  border-radius: 5px;
  text-decoration: none;
  box-shadow: rgb(0, 0, 0) 0px 0px 0px 0px;
  border-radius: 1px;
  transition: 200ms;
  transform: translateY(0);
  display: flex;
  flex-direction: row;
  align-items: center;
  cursor: pointer;
  animation: landing-page-h1 4000ms ease 0s 1 normal forwards;
}
.landing-page__button:hover {
  transition: 196ms;
  padding: 8px 30px;
  transform: translateY(-0px);
  background-color: #fff;
  color: #000000;
  border: solid 2px #000000;
}
.container-bottom-to-up {
  overflow: hidden;
  margin: 0px;
}
@keyframes landing-page-h1 {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}
</style>
