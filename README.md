# 🏠 이집은

![main](https://user-images.githubusercontent.com/116165520/216952191-52be6865-05d4-4c37-a0f3-6524492677f5.png)

[이집은 바로가기](https://www.ezip.store/)
## 📝 목차

[1. 프로젝트 소개](#-프로젝트-소개)<br>
[2. 주요기능](#-주요기능)<br>
[3. 기술적 의사결정](#-기술적-의사결정)<br>
[4. STACK](#-stack)<br>
[5. 팀원소개](#-팀원소개)<br>

### 📢 프로젝트 소개

- 실제 거주 해 본 사람들이 작성하는 찐 리뷰 사이트!
- 집주인도, 중개사도 모르는 진짜 후기를 알려주는 웹서비스 입니다.
- 밤낮, 계절, 날씨, 이웃등의 다양한 변수들은 중개인이나 집주인이 알 수 없어요.
- 정말 살아본 사람들의 이야기를 들을 수 있는 원룸 후기 플랫폼입니다!

### ✨ 주요기능

- 회원가입/로그인 기능
  - 회원가입시 : 원룸 리뷰작성, 커뮤니티 글쓰기, 커뮤니티 댓글쓰기
  - 비회원시 : 지도, 커뮤니티, 댓글 보기만 가능
- 지도 페이지
  - 자동 검색어 기능
  - 지역별 리뷰 개수 파악가능
  - 마커 클릭 시 해당 주소 및 후기 작성 점수 제공
  - 사진 클릭시 확대 및 슬라이드 구현
- 커뮤니티 기능
  - 지역별로 자유롭게 소통하는 페이지
  - 지역별 조회, 검색기능, 최신순, 댓글순 표시
  - 작성된 게시글에 대한 댓글 기능
- 후기작성 페이지
  - 사진 올리고 후기 작성시 지도에 마커 반영

### 💡 기술적 의사결정

- 리액트 쿼리
  - 도입 이유
    - 로그인을 제외한 모든 페이지에서 전역으로 관리할 이유가 없어 캐싱관리를 사용해 API요청의 부담을 덜기 위해 사용
    - 데이터 업데이트 시 빠르게 반영이 된다.
    - 페이징 처리나 지연 로딩 데이터와 같은 성능 최적화를 해준다.
- 리덕스 툴킷
  - 도입 이유
    - Redux—toolkit은 redux의 단점인 보일러플레이트코드와 복잡한 스토어 설정, 페키지설정을 완화시킴
    - 로그인 파트 부분에서 email과 모든 페이지의 로그인 상태 관리 등을 전역으로 관리해야 한다는 생각에 결정
    - Redux—toolkit 사용후 추후에 React-query로 리펙토링 예정
- 리액트 인피니티쿼리
  - 도입 이유
    - react-query를 사용하면서 장점이라고 할 수 있기에 infinitequery를 사용
    - 무한스크롤을 사용하기 위한 observer는 필수라 생각이 들고, 후크를 사용하여 상태를 useInView쉽게 모니터링 할 수 있기 때문

### 💻 STACK

<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=React&logoColor=white"> <img src="https://img.shields.io/badge/ReduxToolkit-764ABC?style=for-the-badge&logo=Redux&logoColor=white"> <img src="https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=Axios&logoColor=white"> <img src="https://img.shields.io/badge/ReactQuery-FF4154?style=for-the-badge&logo=ReactQuery&logoColor=white"> <img src="https://img.shields.io/badge/styledcomponents-DB7093?style=for-the-badge&logo=styled-components&logoColor=white"> <img src="https://img.shields.io/badge/Kakao API-FFCD00?style=for-the-badge&logo=Kakao&logoColor=white"> <img src="https://img.shields.io/badge/AmazonS3-569A31?style=for-the-badge&logo=Amazon-S3&logoColor=white">

### 👪 팀원소개

|              Name(Github)               | Position | Role                                                          |
| :-------------------------------------: | :------- | ------------------------------------------------------------- |
| [이승재](https://github.com/seungjae93) | FE(VL)   | - 지도 페이지<br> - 메인 페이지<br>                           |
|  [조민욱](https://github.com/jominuk)   | FE       | - 커뮤니티 CRUD<br> - 댓글 CRUD <br> - 소셜 로그인(kakao)<br> |
