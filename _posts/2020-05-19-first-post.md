---
title: "라즈베리파이 웹 서비스 호스팅 실습"
date: 2020-05-19 21:08:28 -0000
categories: OSS Raspberrypi Web Service Hosting
---





## 라즈베리파이 웹 서비스 호스팅 실습 ##
<br/>
<br/>
<br/>
1) 라즈베리파이 hostname 바꾸기
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
<img width="715" alt="심볼릭링크생성" src="https://user-images.githubusercontent.com/62292136/82733252-966d2780-9d4d-11ea-928c-b72f766ad311.PNG">
<br/>
웹서비스 세팅 테스트 및 웹서비스 재시작
<br/>
<img width="448" alt="테스트" src="https://user-images.githubusercontent.com/62292136/82733273-b43a8c80-9d4d-11ea-97ce-21ba1c77754e.PNG">
<br/>
<img width="419" alt="재시작" src="https://user-images.githubusercontent.com/62292136/82733275-b7ce1380-9d4d-11ea-91e4-82ba04768d28.PNG">
</br>
</br>
</br>
3) 도메인 이름에 대한 nginx 가상호스트 설정
<br/>
4) 웹 브라우저에서 테스트
<br/>
<br/>
<br/>
<br/>

## 웹 서비스 호스팅 실습 결과 ##

1) ~ 4) 의 내용을 두 번 실행한 후 결과 확인 (사용자 계정 및 도메인 2개 생성)
<br/>
<br/>
첫 번째 세팅한 웹사이트     
Server name : shinhyeongseo.com     
Github Repository :  https://github.com/ShinHyeongSeo/Web-template      
<br/>

<br/>
<br/>
두 번째 세팅한 웹사이트     
Server name : kim.com     
Github Repository : https://github.com/ShinHyeongSeo/github-games      
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

