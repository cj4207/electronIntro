<template>
  <div>
    <div class="items">
      <div class="item">
        <div class="name">이름:</div>
        <div class="value">배찬영</div>
      </div>
      <div class="item">
        <div class="name">생년월일:</div>
        <div class="value">92.12.26 (만 30세)</div>
      </div>
      <div class="item">
        <div class="name">핸드폰:</div>
        <div class="value">010 4533 4607</div>
      </div>
      <div class="item">
        <div class="name">이메일:</div>
        <div class="value">cksdud1226@gmail.com</div>
      </div>
      <div class="item">
        <div class="name">학교:</div>
        <div class="value">금오공과대학교 컴퓨터공학과 졸업</div>
      </div>
      <div class="item">
        <div class="name">취미:</div>
        <div class="value">해외축구, 게임</div>
      </div>
      <div class="item">
        <div class="name">개발 경력:</div>
        <div class="company">
          <div class="company-item">
            <div class="value">뮤팟 - 21.08~23.02 (1년 8개월)</div>
            <span
              class="more"
              v-if="isMoreView1 == false"
              @click="isMoreView1 = true"
              >▼</span
            >
            <span
              class="more"
              v-if="isMoreView1 == true"
              @click="isMoreView1 = false"
              >▲</span
            >
          </div>
          <mewpot-project v-if="isMoreView1 == true"></mewpot-project>
          <div class="company-item">
            <div class="value">아리아엣지 - 23.03~23.05 (3개월)</div>
            <span
              class="more"
              v-if="isMoreView2 == false"
              @click="isMoreView2 = true"
              >▼</span
            >
            <span
              class="more"
              v-if="isMoreView2 == true"
              @click="isMoreView2 = false"
              >▲</span
            >
          </div>
          <aria-project v-if="isMoreView2 == true"></aria-project>
        </div>
      </div>
      <div class="item">
        <div class="name">기타 경력:</div>
        <div class="value">토와한국 - 18.12~21.03 (2년 4개월)</div>
      </div>
      <div class="item">
        <div class="name">교육:</div>
        <div class="value">위코드 부트켐프 21기 수료 - 21.05~21.08</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.title {
  color: #888;
  font-size: 18px;
  font-weight: initial;
  letter-spacing: 0.25px;
  margin-top: 10px;
}
.company-item {
  display: flex;
}
.items {
  margin-top: 8px;
}

.item {
  display: flex;
  margin-bottom: 6px;
}

.item .name {
  color: #6a6a6a;
  margin-right: 6px;
}

.item .value {
  color: #35495e;
  font-weight: bold;
}
.more:hover {
  cursor: pointer;
}
</style>

<script>
import ariaProject from "./ariaProject.vue";
import mewpotProject from "./mewpotProject.vue";

export default {
  components: { ariaProject, mewpotProject },
  data() {
    return {
      isMoreView1: false,
      isMoreView2: false,
    };
  },
};
</script>
