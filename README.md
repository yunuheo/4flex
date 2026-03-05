# 🎥 MovieCaster

영화를 사랑하는 이들을 위한 영화 정보 제공 & 한줄평 작성 웹사이트

✅ **[header]** 유저 상태에 따른 로그인/로그아웃 문구, 홈/로그인 기능

✅ **[메인페이지]** 영화 포스터 클릭 시 상세 페이지로 이동, 코멘트 좋아요 기능, 평점별 날씨 아이콘

✅ **[마이페이지]** 영화/코멘트 좋아요 관리, 내 코멘트 관리

✅ **[상세 페이지]** 영화 정보 조회, 코멘트 작성, 다른 유저의 코멘트 조회 & 비슷한 영화 추천 기능

✅ **[회원가입/로그인]** 유효성검사, ID 찾기

✅ **TMDB API**를 받아와 MySql 데이터 베이스에 저장

- **개발 기간** : 2023-11-07 ~ 2023-11-23(2주)
- **배포 주소** : http://101.101.218.151:8000/
<br />

## 👨‍👩‍👧‍👦 팀 구성

|역할|이름|담당|✍️|
|------|---|---|---|
|Full-stack(조장)|[박윤혜](https://github.com/riverhye)|메인페이지 / API DB저장, 와이어프레임 작성(figma), notion관리|[회고록](https://velog.io/@riverhye/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%EB%B0%9C%ED%91%9C-%ED%94%BC%EB%93%9C%EB%B0%B1)
|Fullstack|[구은현](https://github.com/EunnyKoo)|마이페이지 / 와이어프레임 작성(figma), canva제작 |[회고록](https://velog.io/@eunkoo/2%EC%A3%BC-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%EC%A3%BC%EC%A0%9C-%EC%84%A0%EC%A0%95-%EB%B0%8F-%EC%B4%88%EC%95%88-%EC%9E%91%EC%97%85)|
|Full-stack|[이병진](https://github.com/blee94)|상세페이지 / 와이어프레임 작성(figma)||
|Back-end|[허윤우]()|마이페이지 + 회원가입 로그인 기능 보조, ID 찾기, 발표|[회고록](https://velog.io/@hyoon516/1%EC%B0%A8-%ED%8C%80-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%ED%9A%8C%EA%B3%A0)| 

<br />

# 🔧 개발환경
## Front
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)

## Back
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Sequelize](https://img.shields.io/badge/Sequelize-52B0E7?style=for-the-badge&logo=Sequelize&logoColor=white)

## Environment
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

## Communication & Tool
![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white)
![Canva](https://img.shields.io/badge/Canva-%2300C4CC.svg?style=for-the-badge&logo=Canva&logoColor=white)
![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)

### 그외 사용한 패키지
- swiper.js, axios, ejs, express-session, multer, dotenv

## API
**[TMDB](https://developer.themoviedb.org/reference/intro/getting-started)**(The Movie Database)

<br />

## 🗂️ 디렉토리 구조
```
4FLEX/  
├── config/  
│ ├── envs/  
│ │ └── key.env  
│ └── config.json  
├── controller/  
│ ├── CDetail.js  
│ ├── CFindid.js  
│ ├── CFindpw.js  
│ ├── CGetMovies.js  
│ ├── CMain.js  
│ ├── CMypage.js  
│ ├── CSearch.js  
│ ├── CSignin.js  
│ ├── CSignup.js  
│ ├── CUser.js  
│ └── dummyCmt.js  
├── model/  
│ ├── Comment.js  
│ ├── CommentLike.js  
│ ├── FavMovie.js  
│ ├── getMovie.js  
│ ├── index.js  
│ ├── MovieInfo.js  
│ ├── MovieLike.js  
│ └── User.js  
├── node_modules/  
├── routes/  
│ ├── datail.js  
│ ├── findid.js  
│ ├── findpw.js  
│ ├── indes.js  
│ ├── mypage.js  
│ ├── search.js  
│ ├── signin.js  
│ ├── signout.js  
│ └── signup.js  
├── static/  
│ ├── css/  
│ │ ├── mypage/  
│ │ │ ├── mypage.css  
│ │ │ ├── mypageComment.css  
│ │ │ ├── mypageFav.css  
│ │ │ └── mypageMovieLike.css  
│ │ ├── detail.review.css  
│ │ ├── detail.css  
│ │ ├── findid.css  
│ │ ├── findpw.css  
│ │ ├── footer.css  
│ │ ├── header.css  
│ │ ├── index.css  
│ │ ├── main.css  
│ │ ├── search.css  
│ │ ├── signin.css  
│ │ └── signup.css  
│ └── img/  
├── uploads/  
├── views/  
│ ├── mypage/  
│ │ ├── mypage.ejs  
│ │ ├── mypageComment.ejs  
│ │ ├── mypageCommentLike.ejs  
│ │ ├── mypageFav.ejs  
│ │ ├── mypageInfo.ejs  
│ │ └── mypageMovieLike.ejs  
│ ├── detail.ejs  
│ ├── findid.ejs  
│ ├── findpw.ejs  
│ ├── footer.ejs  
│ ├── header.ejs  
│ ├── main.ejs  
│ ├── search.ejs  
│ ├── signin.ejs  
│ └── signup.ejs  
├── .gitignore  
├── index.js  
├── package-lock.json  
├── package.json  
└── README.md
```

<br />

## 📃 API 명세서
<img width="648" alt="image" src="https://github.com/riverhye/MovieCaster/assets/77149171/9e84ad09-d68e-4540-9306-2cb493c12074">

<br />

## 📋 ERD 다이어그램
<img width="648" alt="image" src="https://github.com/riverhye/MovieCaster/assets/97770736/9a526e45-4c65-4a70-a107-b56cf804e590">

<br />

# 🖥️ 화면 구성 및 주요 기능
## 메인 페이지

![좋아요+main gif](https://github.com/riverhye/MovieCaster/assets/77149171/888a30a6-e008-4ef5-9b5c-15f55d6221b9)

- 헤더 : 유저 상태에 따른 로그인/로그아웃 문구, 홈/로그인 기능
- 최신 영화 : 3초 주기 순위 변경 (1-5위 / 6-10위 반복)
- 평점 높은 영화 : 코멘트 하트 아이콘 클릭 시 좋아요 한 코멘트 추가, 다시 클릭 시 좋아요 삭제 / 슬라이드 기능(swiper.js)
- 평점 2.5~3.5 사이 영화 : 평점별 날씨 아이콘 / 슬라이드 기능(swiper.js)

<br />

## 검색 페이지

![검색 gif](https://github.com/riverhye/MovieCaster/assets/77149171/2f162f54-08e2-494a-8ef5-f3b0e373486d)

- 영화 title 검색 시 결과 개수, 영화 포스터와 title
- 각 영화 포스터 클릭 시 상세 페이지 이동
- 검색 결과 없을 때 검색 결과가 없다는 메시지 화면에 구현
  
<br />

## 상세 페이지
Section1. 한줄평  
여기에서는 해당 영화에 대한 다른 회원들이 작성한 리뷰와 남긴 평점을 볼 수 있습니다.  
만약 로그인을 했다면 직접 리뷰 및 평점을 남길 수 있으며 다른 회원들이 작성한 리뷰에 좋아요을 눌러 마이페이지에서 자신이 좋아요를 누른 리뷰 목록을 불러올 수 있습니다.  
다른 회원들이 본인의 리뷰를 읽어볼 수 있으며 자신이 작성한 평점 또한 바로 반영되어 메인 페이지에서 영화의 순위에 변동이 일어날 수 있습니다.

Section2. 상세내용
여기에서는 영화의 제목, 장르, 줄거리 등 다양한 정보를 제공합니다.  
영화 포스터에 좋아요를 눌러 마이페이지에서 자신이 좋아요를 누른 영화 목록을 불러올 수 있습니다.

Section3. 비슷한 영화 추천  
여기에서는 해당 영화의 장르를 세분화 해 비슷한 장르의 영화를 총 세개 추천하여 표시합니다.
영화의 고유키를 이용하여 각 영화 클릭 시 해당 영화의 상세페이지로 이동이 가능합니다.

<br />

## 마이 페이지(프로필 관리)
![마이페이지1](https://github.com/riverhye/MovieCaster/assets/139302489/418a0309-34ab-49d7-9ba4-8627a6205b1a)
- 회원정보 수정: 프로필 사진, 닉네임, 비밀번호
- 회원정보 탈퇴

<br />

## 마이 페이지(인생작품 등록)
![마이페이지2](https://github.com/riverhye/MovieCaster/assets/139302489/d8533bda-bc16-466d-99d2-243211f56058)
- 영화 제목 검색 시 영화 포스터와 등록 버튼 생성
- 등록 버튼 클릭 시 마이페이지 인생작품 부분에 포스터 등록
- 각 영화 포스터 클릭 시 상세 페이지 이동
<br />

## 마이 페이지(영화/코멘트 좋아요)
![마이페이지3](https://github.com/riverhye/MovieCaster/assets/139302489/b3cdc0ba-d334-407e-bbec-3ccc94a4e5fb)
- 내가 좋아요 누른 영화 확인
- 내가 좋아요 누른 코멘트 작성자와 코멘트 확인
- 좋아요 삭제 가능
<br />
