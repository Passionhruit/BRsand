# [벼랑끝에몰렸조] 샌드위치 주문, 판매관리 웹페이지 벼락샌드

스파르타코딩클럽 6기_React / 23.08.07 ~ 23.08.14 

<div align="center">

[![header](https://capsule-render.vercel.app/api?type=Cylinder&color=B73D52&height=150&section=header&text=벼락%20샌드&fontColor=FFD99B&fontSize=70&animation=fadeIn&fontAlignY=55)
](https://i.ibb.co/dDtQ9H3/2023-08-14-9-44-30.png)
</div>

## 🥪담당기능

- 모바일 메인 페이지[유저] 
- 마이 페이지[유저]
- 결제 페이지[유저] (포트원 구 아임포트 API 사용)
- 주문접수페이지[어드민]

## 목차

-   프로젝트 소개
-   프로젝트 링크
-   기술스택
-   사용한 라이브러리
-   사용한 API
-   버전 관리시스템
-   협업 툴
-   구현 페이지

## 프로젝트 소개

React, TypeScript 를 활용하여 제작한 샌드위치 주문, 판매 관리 웹 애플리케이션 '벼락샌드' 입니다.
지금까지는 유저의 시선에서 웹을 제작했다면, 팀원들과 프로젝트 회의 중, 이번에는 [유저] 와 [어드민] 이 다같이 활용할 수 있는 웹페이지를 만들어보고자 하였습니다.

1-1. [유저] 로그인 : 유저는 보통 모바일이나 키오스크에서 주문을 많이 한다는 특성을 고려해, 모바일에 최적화 된 웹사이트로 제작하였습니다. 주문 전 로그인을 해야하며 로그인 방식은 기본로그인, 간편로그인, 소셜로그인이 있습니다. 유저는 자신의 세부사항 (이름, 성별 등) 을 선택적으로 입력할 수 있습니다.

1-2. [유저] 주문 : 샌드위치 주문 시 기본적으로 입맛에 따라 만드는 커스텀과, 기존에 있는 메뉴를 선택할 수 있는 두가지 방식이 있습니다.

1-3. [유저] 결제 : 결제방식은 현금과 카드 두 가지가 있으며, 아임포트로 연동한 결제방식에 따라 kakaopay 로 결제할 수 있습니다.

1-4. [유저] 마이페이지 : 주문 이후, 유저는 마이페이지로 들어와 자신의 주문상태와 기존에 했던 주문들을 볼 수 있습니다.

2-1. [어드민] 로그인 : 어드민은 최상위 관리자에 의해 데이터베이스로 계정을 생성할 수 있고  회원가입은 따로 존재하지 않습니다.

2-2. [어드민] 주문관리 : 로그인한 어드민은 프라이빗 라우터를 통해 어드민만 접속 가능한 페이지로 이동하게 되는데, 주문 상태관리 페이지는 유저가 한 주문에 대해서 [주문접수대기] -> [주문접수] -> [조리완료] 로 상태 변경을 할 수 있습니다.

이 페이지에서는 재고 관리도 이루어지며, 재고가 20개 미만인 물품에 대해 발주 버튼이 생기고 발주를 누르면 재고가 20개씩 실시간으로 채워지게 됩니다.

2-3. [어드민] 매장관리 : 어드민은 판매한 샌드위치의 해당 지점별 매출을 확인할 수 있습니다. 다른 지점의 매출은 볼 수 없고, 유저가 회원가입시 작성했던 추가 정보에따라 연령대에 따른 판매추이를 확인할 수 있습니다.

3-1. [최상위 어드민] 매장관리 : 전체 매장의 매출통계를 확인할 수 있습니다.

3-2. [최상위 어드민] 멤버관리 : basic, silver, gold 로 각 멤버의 멤버십 등급을 관리할 수 있습니다.


## 프로젝트 링크

https://github.com/projectaub/BRsand

배포: https://b-rsand.vercel.app/
<div align=“center”>
	  <img src="https://img.shields.io/badge/vercel-000000?style=for-the-badge&logo=vercel&logoColor=white">
  </div>

## 기술스택
  * Javascript
  * html/css
  * react
  * TypeScript : 사전에 일어날 가능성이 있는 버그를 막아서 효율적으로 코드 관리를 할 수 있다.
  * Supabase : 다양한 종류의 Data를 다뤄야했기 때문에 백엔드 없이 인증/인가, DB등 다양한 서비스를 제공하기위해 supbase를 사용하였다. Firebase 대비 직관적인 사용 방식으로 팀원 내 만족도가 높았다.
  <div align=“center”>
	  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
    <img src="https://img.shields.io/badge/css3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
  <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white">
  <img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=white">
  <img src="https://img.shields.io/badge/typescript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
 <img src="https://img.shields.io/badge/supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white">     
  </div>
  </div>
  

## 사용한 라이브러리
  * react-router-dom
  * react-swiper
  * styled-component
  * styled-reset
  * nivo-pie
  * react-hook-form

## 사용한 API
  * PG 아임포트 

## 버전 관리 시스템
   * Git/Github
   <div align=“center”>
	  <img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
    <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
  </div>
  
## 협업 툴
  * Visual Studio
  * Slack
  * figma
  * google sheets
<div align=“center”>
	  <img src="https://img.shields.io/badge/visualstudio-5C2D91?style=for-the-badge&logo=visualstudio&logoColor=white">
    <img src="https://img.shields.io/badge/slack-4A154B?style=for-the-badge&logo=slack&logoColor=white">
  <img src="https://img.shields.io/badge/figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white">
  <img src="https://img.shields.io/badge/googlesheets-34A853?style=for-the-badge&logo=googlesheets&logoColor=white">
  </div>
   
## [유저] 모바일 페이지 

TEST ID : test6@naver.com
PASSWORD : 123412

### 1) 메인 페이지

<img width="400" alt="image" src="https://github.com/Passionhruit/BRsand/assets/92542456/62686d5d-82d8-4001-b9ee-f28fb0f3ea78">



### 2) 로그인 페이지

<a href="https://ibb.co/dWZBrfb"><img width="400" src="https://i.ibb.co/sm7j2g5/2023-08-14-10-35-02.png" alt="2023-08-14-10-35-02" border="0"></a>

### 3) 마이페이지

<a href="https://ibb.co/PMJdZmF"><img width="400" src="https://i.ibb.co/DYmZDVz/2023-08-14-9-45-00.png" alt="2023-08-14-9-45-00" border="0"></a>

### 4) 주문 페이지

<a href="https://ibb.co/kXMTVWJ"><img width="400" src="https://i.ibb.co/CQWypT6/2023-08-14-9-45-30.png" alt="2023-08-14-9-45-30" border="0"></a>
<a href="https://ibb.co/q9pDsQZ"><img width="400" src="https://i.ibb.co/mt4RqWx/2023-08-14-9-45-44.png" alt="2023-08-14-9-45-44" border="0"></a>

### 5) 결제 페이지

<a href="https://ibb.co/7KXSsr7"><img width="400" src="https://i.ibb.co/NKsFcWw/2023-08-14-9-45-59.png" alt="2023-08-14-9-45-59" border="0"></a>


## [어드민] 웹 페이지 https://b-rsand-inky.vercel.app/admin

TEST ID : manager1@test.com
PASSWORD : 111111


### 1) 메인 페이지

<a href="https://ibb.co/WFHrTxt"><img src="https://i.ibb.co/Cvwjr12/2023-08-14-9-46-30.png" alt="2023-08-14-9-46-30" border="0"></a>


### 2) 주문관리 페이지

<a href="https://ibb.co/mS0zNKD"><img src="https://i.ibb.co/x3Y5FbC/2023-08-14-9-46-51.png" alt="2023-08-14-9-46-51" border="0"></a>


### 3) 매장관리 페이지

<a href="https://ibb.co/WtMd82x"><img src="https://i.ibb.co/9t1fKr8/2023-08-14-9-47-12.png" alt="2023-08-14-9-47-12" border="0"></a>

### 4) 회원관리 페이지

<a href="https://ibb.co/mvp2bqh"><img src="https://i.ibb.co/z8dBQRP/2023-08-14-10-09-47.png" alt="2023-08-14-10-09-47" border="0"></a>
