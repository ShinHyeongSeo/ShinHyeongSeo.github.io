---
title: "라즈베리파이 웹 서비스 호스팅 실습"
date: 2020-05-19 21:08:28 -0000
categories: OSS Raspberrypi Web Service Hosting
---





## 라즈베리파이 웹 서비스 호스팅 실습 ##
<br/>
<br/>
1) 라즈베리파이 hostname 바꾸기
<br/>
<br/>
sudo su - 명령어를 통해 슈퍼유저 되고난 후     
raspi-config 명령어를 통해 라즈베리파이 환경설정 탭에 진입
<br/>
<img width="579" alt="hostname바꾸기0" src="https://user-images.githubusercontent.com/62292136/82732973-a126bd00-9d4b-11ea-949b-5e7534046682.PNG">
<br/>
<img width="578" alt="hostname바꾸기1" src="https://user-images.githubusercontent.com/62292136/82732976-a257ea00-9d4b-11ea-8ca3-7c76a196843d.PNG">
<br/>
<br/>
차례로 Network Options, Hostname 탭을 선택한 후 pi이름을 변경
<br/>
<img width="485" alt="hostname바꾸기0 5" src="https://user-images.githubusercontent.com/62292136/82733071-5c4f5600-9d4c-11ea-9ca8-18692531c6de.PNG">
<br/>
<img width="580" alt="hostname바꾸기2" src="https://user-images.githubusercontent.com/62292136/82732978-a257ea00-9d4b-11ea-8415-ca88b4983fbc.PNG">
<br/>
<img width="579" alt="hostname바꾸기3" src="https://user-images.githubusercontent.com/62292136/82732979-a2f08080-9d4b-11ea-81ef-ae33f70415c1.PNG">
<br/>
<br/>
hostname이 잘 변경되었는지 확인
<br/>
<img width="828" alt="hostname바꾸기4" src="https://user-images.githubusercontent.com/62292136/82732980-a2f08080-9d4b-11ea-97f6-f91361438492.PNG">
<br/>
<br/>
<br/>
2) 사용자 계정 생성 및 도메인 이름 설정
<br/>
<br/>
sudo su - 명령어를 통해 슈퍼유저 되고난 후,      
useradd -m "유저이름"과 passwd "유저이름" 명령어를 통해 사용자 추가 및 비밀번호 생성 실행
<br/>
<img width="581" alt="사용자추가" src="https://user-images.githubusercontent.com/62292136/82733149-f6170300-9d4c-11ea-878f-3d4d0619b171.PNG">
<br/>
<br/>
웹사이트 세팅파일 제작
<br/>
<img width="565" alt="웹사이트세팅파일제작" src="https://user-images.githubusercontent.com/62292136/82733233-72a9e180-9d4d-11ea-97cc-f7fc34c81ace.PNG">
<br/>
심볼릭 링크 제작
<br/>
<img width="715" height="50" alt="심볼릭링크생성" src="https://user-images.githubusercontent.com/62292136/82733252-966d2780-9d4d-11ea-928c-b72f766ad311.PNG">
<br/>
웹서비스 세팅 테스트 및 웹서비스 재시작
<br/>
<img width="715" height="50" alt="테스트" src="https://user-images.githubusercontent.com/62292136/82733273-b43a8c80-9d4d-11ea-97ce-21ba1c77754e.PNG">
<br/>
<img width="715" height="50" alt="재시작" src="https://user-images.githubusercontent.com/62292136/82733275-b7ce1380-9d4d-11ea-91e4-82ba04768d28.PNG">
<br/>
<br/>
<br/>
3) 도메인 이름에 대한 nginx 가상호스트 설정
<br/>
<br/>
로컬PC의 hotst 파일에 부여받은 도메인과 IP주소를 추가
<br/>
<img width="516" alt="hosts파일12" src="https://user-images.githubusercontent.com/62292136/82748382-54d78d80-9ddc-11ea-9887-fad93cec4936.PNG">
<br/>
<br/>
새롭게 생성된 사용자 계정으로 로그인
<br/>
<img width="579" alt="새계정로그인" src="https://user-images.githubusercontent.com/62292136/82748353-1641d300-9ddc-11ea-9f79-3697725bdc1b.PNG">
<br/>
<br/>
간단한 웹페이지 만들어 추가하기
<br/>
<img width="445" alt="페이지만들기" src="https://user-images.githubusercontent.com/62292136/82748404-83556880-9ddc-11ea-8206-ce79184b8bf5.PNG">
<br/>
<br/>
<br/>
4) 웹 브라우저에서 테스트
<br/>
<br/>
<img width="960" alt="웹페이지테스트" src="https://user-images.githubusercontent.com/62292136/82748418-a54eeb00-9ddc-11ea-97c8-b8ee950ae4b0.PNG">
<br/>
<br/>
<br/>
<br/>
## 웹 서비스 호스팅 실습 결과 ##
<br/>
<br/>
2) ~ 4) 의 내용을 두 번 실행한 후 결과 확인 (사용자 계정 및 도메인 2개 생성)
<br/>
<br/>
각 호스트의 웹페이지를 GitHub에서 적절한 웹사이트를 fork clone하여 제작
<br/>
<br/>
내용을 수정하고 add commit push를 통해 Github Repository에 commit 반영 확인
<br/>
첫 번째 세팅한 웹사이트     
Server name : shinhyeongseo.com     
Github Repository :  https://github.com/ShinHyeongSeo/Web-template      
라즈베리파이 내 디렉토리 : /etc/nginx/sites-available/shinhyeongseo.com
<br/>
<br/>
<br/>
Github Repository
<br/>
<br/>
원래 웹사이트 캡처 이미지
<br/>
<br/>
웹 사이트 내용 수정
<br/>
<br/>
add commit push
<br/>
<br/>
Github Repository commit 반영 확인
<br/>
<br/>
바뀐 웹사이트 캡처 이미지
<br/>
<br/>
<br/>
<br/>
두 번째 세팅한 웹사이트     
Server name : kim.com     
Github Repository : https://github.com/ShinHyeongSeo/github-games     
라즈베리파이 내 디렉토리 : /etc/nginx/sites-available/kim.com      
<br/>
<br/>
<br/>
Github Repository
<br/>
<br/>
원래 웹사이트 캡처 이미지
<br/>
<br/>
웹 사이트 내용 수정
<br/>
<br/>
add commit push
<br/>
<br/>
Github Repository commit 반영 확인
<br/>
<br/>
바뀐 웹사이트 캡처 이미지
<br/>
<br/>
<br/>
<br/>

