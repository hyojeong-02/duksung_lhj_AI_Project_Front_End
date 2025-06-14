# 인터넷 기초[04] 과제2 - 나만의 인공지능 서비스

## 🧾 개요
- **서비스 명** : 오늘 뭐 먹지? - AI 식사 추천
- **서비스 설명** : 사용자가 음식 종류, 아침•점심•저녁 시간대, 날짜를 입력하면 AI가 오늘 먹으면 좋을 음식을 추천해준다.
- **서비스 접속 주소** : [https://hyojeong-02.github.io/duksung_lhj_AI_Project_Front_End/](https://hyojeong-02.github.io/duksung_lhj_AI_Project_Front_End/)


## ⚙️ 서비스 구성 요소(1) - Gemini API
- AI가 추천하는 음식은 Google의 대형언어모델(Large Multimodal Model)인 Gemini API를 통해 생성된다.
- **활용 모델** : `Gemini-2.0-flash`
- **시스템 프롬프트 주안점**
  - 사용자가 선택한 음식 종류, 시간대, 날짜를 바탕으로 적절한 음식을 유머있고 친근하게 추천하도록 유도
  - 특히! 날짜별로 계절 추천 메뉴를 선택해줌


## 서비스 구성 요소(2) - 프론트엔드
- <span style="background-color:rgb(182,0,80)">오늘 뭐 먹지?</span> 서비스 페이지는 HTML, CSS, JavaScript를 사용하여 간단하게 구성하였다.
- CSS 스타일 시트는 [style.css](style.css)파일로 따로 분리하였다.
- 대표이미지는 Chat GPT를 이용하여 생성하였다.<br>
<img src="./images/main.webp" width="200px" height="200px">


## 서비스 구성 요소(3) - 백엔드
- Gemini API 키 보호를 위해 별도의 백엔드 서버를 구현하고, 프론트엔드 요청을 중계하는 구조로 설계하였다.
- 해당 백엔드는 Vercel의 서버리스 함수(Serverless Function) 기능을 이용해 배포하였다.
- 구현 코드는 다음 저장소에서 확인할 수 있다:  
  [https://github.com/hyojeong-02/duksung_lhj_AI_Project_api](https://github.com/hyojeong-02/duksung_lhj_AI_Project_api)
