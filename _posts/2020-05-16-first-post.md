---
title: "라즈베리파이 웹 서비스 세팅 실습"
date: 2020-05-16 21:04:28 -0000
categories: OSS Raspberrypi Web page Service
---




## 라즈베리파이 웹 서비스 세팅 실습 ##

### 1. 라즈베리파이 세팅 ###

1) 먼저 라즈베리파이에서 사용할 OS image file을 다운받습니다.        
https://raspberrypi.org 사이트접속 -> Download 탭 -> Raspbian 선택 ->         
Raspbian Buster with desktop and recommended software 다운로드     
(로컬 디스크 C처럼 폴더가 한글명이 포함되지 않은 곳에 다운로드 하는 것을 추천)     
     
2) 라즈베리파이 Imager를 설치해줍니다.     
https://raspberrypi.org 사이트 접속 -> Download 탭 -> Raspberrypi Imager for(운영체제) 다운로드 후 설치     
     
     
     
3) 프로그램을 이용해 MicroSD memory를 포맷합니다.     
Raspberrypi Imager 실행 -> SD Card 선택 -> CHOOSE OS 탭에서 Erase 선택 -> WRITE         

      
      
4) 프로그램을 이용해 MicroSD memory에 OS image file을 설치합니다.     
Raspberrypi Imager 실행 -> SD Card 선택 -> CHOOSE OS 탭에서 Use Custom 선택 ->
다운로드 받은 OS Image 압축파일 선택 -> Write     
       
5) ssh 파일과 (wifi를 이용하는 경우) wpa_supplicant.conf 파일을 작성하여 MicroSD memory에 저장합니다.     
ssh 파일 : 이름이 ssh인 내용이 없는 파일 만들기     
wpa_supplicant.conf 파일     
     
      
6) MicroSD memory를 컴퓨터에서 분리해 라즈베리파이에 꽂아주고 전원을 켭니다.       
      
       
       
       
        
       
### 2. 라즈베리파이를 통한 웹서비스 세팅 ###
     
1) 라즈베리파이의 IP주소 찾기     
cmd에서 ping raspberrypi.local 명령어를 통해 찾기     
만약 안될 시, 공유기 관리자모드로 접속해 라즈베리파이 아이피를 찾는다.     
     
     
     
2) Putty를 통해 라즈베리파이를 ssh로 접속 후 로그인     
username : pi     
password : raspberry     
     
     
     
     
3) nginx 웹서버 설치      
sudo su - 명령어를 통해 슈퍼유저 되고난 후     
apt-get update 명령어를 통해 라즈베리파이 최신 버전으로 업데이트 후     
apt-get install nginx 명령어를 통해 nginx web server 설치     
     
     
     
     
4) 웹서비스 시작     
service nginx start 명령어를 통해 웹서비스 시작 후 확인     
     
     
     
5) 새로운 웹페이지 추가     
/var/www/html 폴더로 이동 후 index.html 파일 생성 후 추가     
      
      
     
      
6) 라즈베리파이 웹서버 페이지로 가서 확인     
     
     
     
     

