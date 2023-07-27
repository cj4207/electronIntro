<template>
  <div>
    <div class="items">
      <h3 class="project-first">C#기반 WFP 프로그램 Electron 이전</h3>
      <ul>
        <li>기술 스택</li>
        <p>React, Electron, amqplib, opencv4nodejs</p>
        <li>시리얼 통신</li>
        <p>시리얼 통신으로 아두이노(자동문) 연결</p>
        <p>자동문 open/close 제어</p>
        <li>메세지 큐</li>
        <p>메세지 큐로 서버와 통신후 자동문 제어 ( 순서 부여 )</p>
        <p>작업자의 복장 검출 내용 서버 전달 - 이미지 첨부</p>
        <li>디바이스 연결</li>
        <p>홍채 인식기, 경광봉, 카메라 모듈 연결</p>
        <p>홍채 인식기 연결에 필요한 dll 파일 연결</p>
        <p>홍채 인식기 데이터 호출을 위한 함수 구현 (c#)</p>
        <li>AI 학습 모델 연동</li>
        <p>복장 검출 학습 모델 electron에 연동</p>
        <p>복장 검출을 위한 openCV 사용</p>
        <p>복장 검출에 따라 키오스크에 rect drawing</p>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.items {
  color: #2c3e50;
}
li {
  font-weight: 700;
}
.project-first {
  border-bottom: solid 2px;
}
</style>
