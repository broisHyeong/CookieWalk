# cookiewalk
<img src="https://github.com/user-attachments/assets/dd838b43-f07f-4a0e-8627-fcfd102ecd32" alt="logo" width="200" height="200"/>

디지털스마트 부산 아카데미 웹개발 프로젝트 

개발기간: 2024.03.10 ~ 2024.06.20

## cookiewalk 개발배경


서구화된 식단과 운동량 감소로 인해 비만율이 증가하고 있습니다. 비만율의 증가는 건강 악화, 사회적 비용 증가, 그리고 기형아 출산율 증가 등 다양한 문제를 초래합니다. 쿠키워크는 이러한 사회 문제를 인식하고, 운동량을 늘리기 위해 개발된 앱입니다.


우선, 현대인들이 운동을 하지 않는 이유에 대한 배경 조사가 필요했습니다.


**잡코리아에서 조사한 직장인들이 운동을 안하는 이유**


1. 게을러서 행동으로 이어지지 않음
2. 시간이 없어서
3. 흥미를 느끼지 못해서
4. 경제적인 여유가 부족해서

위 4가지 이유는 비중이 큰 순서대로 나열하였습니다.


현대인들이 운동을 하지 않는 이유들을 해결하기 위해 팀원들과 깊이 토의한 결과, 가장 접근하기 쉬운 운동인 걷기를 선택했습니다.

걷기는 심혈관 건강 증진, 혈압 및 혈당 조절, 척추를 지지하는 근육 발달, 신경세포 활성화를 통한 스트레스와 우울증 감소 등 많은 운동 효과를 가지고 있습니다.


### 걷기를 어떻게 재밌게 할 수 있을까?

![화면 캡처 2024-07-29 203616](https://github.com/user-attachments/assets/08d0c071-2203-4d44-b16b-21cab4b15866)

우리는 위의 사진에서 영감을 받아, 사용자 주변의 산책 경로를 그림처럼 만들면 걷기에 더 흥미를 느낄 수 있을 것이라고 생각했습니다. 이를 바탕으로 쿠키워크 앱을 제작하게 되었습니다.


---

## 기술스택
**Environment** 

<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=Git&logoColor=white"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=GitHub&logoColor=white"> 

**Config**  
<img src="https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white"> 

**Development** 

<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=React&logoColor=white"><img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=Node.js&logoColor=white"> <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=Supabase&logoColor=white"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScripts&logoColor=white"> 

---
## 시스템 구현 과정
![image01](https://github.com/user-attachments/assets/1a0644fc-8c8f-44a5-865f-ecfc4f8483e8) 

팀원 모두가 Java와 Kotlin에 대한 지식이 없었기 때문에, 웹뷰(WebView)를 활용하여 앱을 제작하는 방식을 선택했습니다. 이 과정에서 GitHub와 연동하여 Netlify에서 사이트를 빌드하고, SWING2APP을 통해 Netlify에서 배포된 URL을 기반으로 APK 파일을 생성할 수 있었습니다.


## 화면구성 및 주요기능 

**홈페이지** 

<img src="https://github.com/user-attachments/assets/74826d51-7710-424c-a0ec-7934f143f0b1" width="200">

* 사용자들이 자유롭게 게시글을 올릴 수 있는 커뮤니티 공간입니다.
* 게시글은 일반적인 이미지와 사용자가 완료한 경로를 올릴 수 있습니다.
* 사용자들은 게시된 게시글에 좋아요나 댓글을 입력할 수 있습니다. 또한 타 사용자 프로필 이미지를 클릭시 해당 사용자의 프로필에 들어가 팔로우 기능을 이용할 수 있습니다.

---
**맵페이지** 

<img src="https://github.com/user-attachments/assets/f19b4849-731f-4959-9a77-5850a88f8491" width="200">

* 사용자들의 주변에 따라걸을 경로를 검색할 수 있는 페이지입니다.
* 초기는 거리가 가장 가까운 순으로 지도가 나열됩니다.
* 지역, 거리, 난이도 별로 필터링이 가능하며 위치나 제목을 검색창에 입력하여 경로를 조회할 수 있습니다.
* 또한 사용자들이 직접 경로를 그릴 수 있으며 원하는 색상 또한 선택할 수 있습니다.

---
**걷기페이지** 

<img src="https://github.com/user-attachments/assets/62f19cce-f30f-4761-b461-8ec898ea55da" width="200"> 

* 경로를 선택하여 걷는 경우, 지도에 가상의 선이 그어집니다. 그어진 선 사이로 여러 점들이 있는데 사용자가 점과 점사이를 통과해 걸으면 선의 색이 진해지며 점과 점사이를 이을 수 있습니다.
* 구글 TTS API를 이용하여 다음 포인트가 좌회전, 우회전, 유턴의 방향전환이 있을 시 음성으로 안내해 주어 사용자가 지속적으로 화면을 보지 않고도 산책이 가능하게 하였습니다.
* 산책의 흥미를 더하기 위해 500m 걸을 시 포인트를 제공하고 있습니다. 이 포인트는 앱의 캐릭터 구매, 기프티콘 구매등으로 활용할 수 있습니다.
---
**그룹페이지**

<img src="https://github.com/user-attachments/assets/65c94930-41ab-4165-b7d1-5c9935e1d518" width="200"> 

* 사용자들이 그룹을 만들고 협력하여 그릴 수 있는 페이지 입니다.
* 그룹 조회를 통해 원하는 그룹을 선택하고 참여할 수 있습니다.
* 최대 5명까지 가능하며, 한 경로를 중복 선택은 불가능합니다.
* 혼자 걷는 경로는 한 붓그리기 형식이었으나, 그룹은 각 경로마다 따로 시작점을 설정 할 수 있어 좀 더 다채로운 그림을 그릴 수 있습니다.

---
**마이페이지** 

<img src="https://github.com/user-attachments/assets/596dcbd3-3558-42c5-9108-04af7639d176" width="200"> 

* 사용자의 정보를 확인할 수 있는 페이지입니다.
* 프로필사진, 닉네임, 코멘트 등을 수정할 수 있습니다.
* 그래프를 통해 주,월,년 별로 사용자의 경로 기록을 확인할 수 있습니다.
* 완성한 경로를 확인할 수 있고 상점으로 이동해 아바타나 여러 상품들을 구매 할 수 있습니다.

## 포스터

[![2조 포스터_최종](https://github.com/user-attachments/assets/948246ec-4208-4292-a439-2c3930df30aa)](https://github.com/user-attachments/files/16435506/2._.pdf) 

(클릭하시면 pdf 다운 가능합니다!)

## 시연영상  

[![디지털 스마트 부산 4기 - 쿠키워크팀 시연영상](https://img.youtube.com/vi/3zDU3z1x_DU/0.jpg)](https://www.youtube.com/watch?v=3zDU3z1x_DU)

## 역할

저는 이번 프로젝트에서 프론트엔드를 담당하였습니다. 주요 작업은 다음과 같습니다:

* **페이지 레이아웃 제작**: Figma를 이용하여 웹 페이지의 디자인과 레이아웃을 설계했습니다.
* **구체적인 웹 제작**: React를 이용하여 설계한 디자인을 실제 웹 애플리케이션으로 구현했습니다.
* **발표 자료 준비**: 프로젝트의 주요 내용을 정리하여 PPT를 제작했습니다.
* **포스터 제작**: 프로젝트의 개요와 성과를 시각적으로 표현한 포스터를 제작했습니다.
* **시연 영상 제작**: 프로젝트의 동작 과정을 보여주는 시연 영상을 제작했습니다.
* **최종 발표**: 팀을 대표하여 최종 발표를 진행하였습니다.


## 개선하고 싶은 점



클라이언트,서버 동시 실행 시키는 법
1.현재 디렉터리 server로 변경 cd server
2.npm run start 

서버만 실행 시키려면
1.현재 디렉터리 server  cd server
2.nodemon server.js    or   npm run server

*cd server에서 npm run client해서 클라만 실행 가능

