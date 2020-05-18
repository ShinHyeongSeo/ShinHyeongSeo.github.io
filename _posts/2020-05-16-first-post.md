---
title: "라즈베리파이 웹 서비스 세팅 실습"
date: 2020-05-16 21:04:28 -0000
categories: OSS Raspberrypi Web page Service
---
                 
                 
                 
                 
                 
                 
                 
                 
                 



## 라즈베리파이 웹 서비스 세팅 실습 ##
<br/>         
<br/>    
<br/>    
<br/>    
<br/>    
<br/>    
         
### 1. 라즈베리파이 세팅 ###

1) 먼저 라즈베리파이에서 사용할 OS image file을 다운받습니다.        
https://raspberrypi.org 사이트접속 -> Download 탭 -> Raspbian 선택              
-> Raspbian Buster with desktop and recommended software 다운로드     
(로컬 디스크 C처럼 폴더가 한글명이 포함되지 않은 곳에 다운로드 하는 것을 추천)     
<img width="949" alt="이미지파일다운로드1" src="https://user-images.githubusercontent.com/62292136/82210889-db0e5280-994a-11ea-9327-79017e8cd545.PNG">     
<img width="388" alt="이미지파일다운로드2" src="https://user-images.githubusercontent.com/62292136/82210893-dcd81600-994a-11ea-8eba-e56b2c3c07fa.PNG">     
     
     
     
2) 라즈베리파이 Imager를 설치해줍니다.     
https://raspberrypi.org 사이트 접속 -> Download 탭 -> Raspberrypi Imager for(운영체제) 다운로드 후 설치     
<img width="960" alt="imager다운로드" src="https://user-images.githubusercontent.com/62292136/82210885-d8abf880-994a-11ea-8d0b-befab51e37a3.PNG">      
       
       
     
3) 프로그램을 이용해 MicroSD memory를 포맷합니다.     
Raspberrypi Imager 실행 -> SD Card 선택 -> CHOOSE OS 탭에서 Erase 선택 -> WRITE         
     
      
      
4) 프로그램을 이용해 MicroSD memory에 OS image file을 설치합니다.     
Raspberrypi Imager 실행 -> SD Card 선택 -> CHOOSE OS 탭에서 Use Custom 선택     
-> 다운로드 받은 OS Image 압축파일 선택 -> Write     
       
       
       
5) ssh 파일과 (wifi를 이용하는 경우) wpa_supplicant.conf 파일을 작성하여 MicroSD memory에 저장합니다.     
ssh 파일 : 이름이 ssh인 내용이 없는 파일 만들기     
wpa_supplicant.conf 파일     
<img width="422" alt="wpa_supplicant파일" src="https://user-images.githubusercontent.com/62292136/82210980-08f39700-994b-11ea-8583-8f37a26ef9fd.PNG">     
     
     
      
6) MicroSD memory를 컴퓨터에서 분리해 라즈베리파이에 꽂아주고 전원을 켭니다.       
       
       
       
       
        
       
### 2. 라즈베리파이를 통한 웹서비스 세팅 ###
     
1) 라즈베리파이의 IP주소 찾기     
cmd에서 ping raspberrypi.local 명령어를 통해 찾기     
만약 안될 시, 공유기 관리자모드로 접속해 라즈베리파이 아이피를 찾는다.     
<img width="813" alt="라즈베리파이ip주소" src="https://user-images.githubusercontent.com/62292136/82211008-190b7680-994b-11ea-8c9b-d751f5c9e94b.PNG">      
     
     
     
2) Putty를 통해 라즈베리파이를 ssh로 접속 후 로그인     
username : pi     
password : raspberry     
<img width="339" alt="putty" src="https://user-images.githubusercontent.com/62292136/82211034-258fcf00-994b-11ea-9e94-59ad504dfe9a.PNG">     
<img width="612" alt="로그인성공" src="https://user-images.githubusercontent.com/62292136/82211044-2a548300-994b-11ea-8dd4-d16b1f858976.PNG">       
     
     
     
3) nginx 웹서버 설치      
sudo su - 명령어를 통해 슈퍼유저 되고난 후     
<img width="670" alt="슈퍼유저되기" src="https://user-images.githubusercontent.com/62292136/82211103-45bf8e00-994b-11ea-824b-8064cb27a745.PNG">     
     
apt-get update 명령어를 통해 라즈베리파이 최신 버전으로 업데이트 후     
<img width="670" alt="apt-get_update" src="https://user-images.githubusercontent.com/62292136/82211113-4a844200-994b-11ea-9d9e-5d6d532910c7.PNG">      
      
apt-get install nginx 명령어를 통해 nginx web server 설치     
<img width="948" alt="ningx_설치1" src="https://user-images.githubusercontent.com/62292136/82211154-5d971200-994b-11ea-9e54-d0d1978c1549.PNG">     
<img width="948" alt="ningx_설치2" src="https://user-images.githubusercontent.com/62292136/82211155-5ec83f00-994b-11ea-85af-455f3910257c.PNG">       
<img width="948" alt="ningx_설치3" src="https://user-images.githubusercontent.com/62292136/82211157-5f60d580-994b-11ea-873d-a93a00c882a6.PNG">       
      
      
     
4) 웹서비스 시작     
service nginx start 명령어를 통해 웹서비스 시작 후 확인     
<img width="960" alt="웹서비스시작" src="https://user-images.githubusercontent.com/62292136/82211330-a8b12500-994b-11ea-8310-b9fef02e0fe0.PNG">      
     
     
     
5) 새로운 웹페이지 추가     
/var/www/html 폴더로 이동 후 index.html 파일 생성 후 추가     
<img width="604" alt="index html_추가" src="https://user-images.githubusercontent.com/62292136/82211260-8f0fdd80-994b-11ea-8c7a-4b3ccd10d67c.PNG">      
     
      
       
6) 라즈베리파이 웹서버 페이지로 가서 확인     
<img width="960" alt="웹서비스수정" src="https://user-images.githubusercontent.com/62292136/82211333-a9e25200-994b-11ea-971f-08cbdbae4618.PNG">       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       
       

     
     
     
     

