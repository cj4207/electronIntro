<template>
  <div id="wrapper">
    <div class="black-bg" v-if="isModal == true">
      <div class="white-bg">
        <button class="close" @click="isModal = false">닫기</button>
        <introduce></introduce>
      </div>
    </div>
    <main>
      <div class="left-side">
        <div>
          <span class="title" @click="isModal = true">
            안녕하세요. 프론트개발자 배찬영입니다. (자세히 보기)
          </span>
        </div>
        <my-information></my-information>
      </div>
      <img
        id="myPhoto"
        src="~@/assets/KakaoTalk_Photo_2021-06-20-19-45-13.jpeg"
        alt="electron-vue"
      />
    </main>
  </div>
</template>

<script>
import myInformation from "./LandingPage/myInformation";
import introduce from "./LandingPage/introduce.vue";

export default {
  name: "landing-page",
  components: { myInformation, introduce },
  data() {
    return {
      isModal: false,
    };
  },
  methods: {
    open(link) {
      this.$electron.shell.openExternal(link);
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Source+Sans+Pro");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "Source Sans Pro", sans-serif;
  margin: 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  position: absolute;
  left: 0px;
  top: 0px;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  padding: 20px;
}
.white-bg {
  position: relative;
  width: 80%;
  background: white;
  border-radius: 8px;
  padding: 20px;
  margin: 0 auto;
}
.close {
  position: absolute;
  right: 10px;
  top: 10px;
  padding: 5px;
}
#wrapper {
  background: radial-gradient(
    ellipse at top left,
    rgba(255, 255, 255, 1) 40%,
    rgba(229, 229, 229, 0.9) 100%
  );
  /* height: 100vh; */
  padding: 60px 80px;
  width: 100vw;
}

#myPhoto {
  /* display: flex; */
  height: 420px;
  margin-bottom: 20px;
  width: 420px;
}

main {
  display: flex;
  justify-content: space-between;
}

main > div {
  flex-basis: 50%;
}

.left-side {
  display: flex;
  flex-direction: column;
}

.welcome {
  color: #555;
  font-size: 23px;
  margin-bottom: 10px;
}

.title {
  display: inline;
  color: #2c3e50;
  font-size: 20px;
  font-weight: bold;
  margin-bottom: 6px;
}

.title:hover {
  color: #5a81a8;
  cursor: pointer;
}

.title.alt {
  font-size: 18px;
  margin-bottom: 10px;
}

.doc p {
  color: black;
  margin-bottom: 10px;
}

.doc button {
  font-size: 0.8em;
  cursor: pointer;
  outline: none;
  padding: 0.75em 2em;
  border-radius: 2em;
  display: inline-block;
  color: #fff;
  background-color: #4fc08d;
  transition: all 0.15s ease;
  box-sizing: border-box;
  border: 1px solid #4fc08d;
}

.doc button.alt {
  color: #42b983;
  background-color: transparent;
}
</style>
