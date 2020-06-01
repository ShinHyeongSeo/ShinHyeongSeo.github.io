---
title: "Batflat 블로그 설치"
date: 2020-05-26 23:22:28 -0000
categories: OSS Batflat Web Service Hosting
---




## Batflat 블로그 설치 실습 ##
<br/>
<br/>
본 실습은 라즈베리파이에 블로그용 가상호스트를 세팅하고 블로그를 개설하는 실습입니다.
<br/>
<br/>
1) Nginx HTTP Server 설치
<br/>
<br/>
라즈베리파이의 관리자 계정으로 로그인한 후
<br/>
sudo su - 명령어를 통해 슈퍼유저가 된다.
<br/>
apt update
<br/>
apt install nginx
<br/>
<br/>
service nginx restart
<br/>
위의 명령어를 실행시켜서 nginx HTTP Server를 설치한다.
<br/>
<br/>
<img width="581" alt="http_server설치1" src="https://user-images.githubusercontent.com/62292136/83344976-d1242080-a348-11ea-9a23-33817244422d.PNG">
<br/>
<br/>
<br/>
2) PHP 7.3과 관련된 모듈 설치
<br/>
<br/>
이 역시 관리자 계정의 슈퍼유저가 된 후
<br/>
<br/>
apt install software-properties-common
<br/>
apt update
<br/>
apt install php7.3-fpm php7.3-common php7.3-mbstring php7.3-xmlrpc php7.3-sqlite3 php7.3-soap php7.3-gd php7.3-sml php7.3-cli php7.3-curl php7.3-zip
<br/>
<br/>
위의 명령들을 실행시켜서 PHP7.3과 관련 모듈을 설치한다.
<br/>
<br/>
<br/>
<img width="516" alt="http_server설치2" src="https://user-images.githubusercontent.com/62292136/83345022-3aa42f00-a349-11ea-940e-70dfafab84a6.PNG">
<br/>
<br/>
<img width="534" alt="http_server설치4" src="https://user-images.githubusercontent.com/62292136/83345029-54de0d00-a349-11ea-98a3-91a1fcd4b6d3.PNG">
<br/>
<br/>
<br/>
3) 블로그용 가상 호스트 세팅하기
<br/>
<br/>
cd /etc/nginx/sites-available 명령어를 통해 해당 디렉토리로 이동한다.
<br/>
<br/>
vi myblog.com 명령어를 통해 웹서비스 세팅파일을 작성한다.
<br/>
<br/>
세팅파일 내용
<br/>
도메인 : myblog.com     
사용자 : shinhyeongseo     
도큐먼트 홈 : /home/shinhyeongseo/html/blog
<br/>
<br/>
<img width="522" alt="세팅파일" src="https://user-images.githubusercontent.com/62292136/83345034-73440880-a349-11ea-985d-920c763492b0.PNG">
<br/>
<br/>
<br/>
cd /etc/nginx/sites-enabled 명령어를 통해 해당 디렉토리로 이동한다.
<br/>
<br/>
ln -s /etc/nginx/sites-available/myblog.com myblog.com
<br/>
해당 명령어를 통해 심볼릭 링크를 생성한다.
<br/>
<br/>
nginx -t
<br/>
service nginx restart
<br/>
명령어를 통해 nginx를 재시작한다.
<br/>
<br/>
윈도우의 경우 hosts파일을 수정해준다.
<br/>
<br/>
<img width="568" alt="hosts파일" src="https://user-images.githubusercontent.com/62292136/83345046-848d1500-a349-11ea-8fc4-b858eb3297c1.PNG">
<br/>
<br/>
<br/>
4) Batflat 최신버전 다운받기
<br/>
<br/>
위에서 세팅한 블로그용 가상호스트 사용자 계정으로 로그인한다.
<br/>
<br/>
cd ~/html 명령어를 통해 해당 디렉토리로 이동한다.
<br/>
<br/>
wget https://github.com/sruupl/batflat/archive/master.zip      
명령어를 통해 해당사이트에서 파일을 디렉토리에 다운받는다.
<br/>
<br/>
unzip master.zip 명령어를 통해      
압축파일을 푼다.
<br/>
<br/>
mv batflat-master blog 명령어를 통해     
블로그 파일이 저장되어있는 디렉토리의 이름을 수정한다.
<br/>
<br/>
mkdir ./tmp     
mkdir ./admin/tmp     
명령어를 통해 디렉토리를 생성한다.
<br/>
<br/>
chmod -R 777 ./uploads ./inc/data ./admin/tmp ./tmp     
위의 명령어를 통해 해당 디렉토리의 권한을 바꿔준다.
<br/>
<br/>
<br/>
<img width="747" alt="새계정로그인후_batflat다운로드1" src="https://user-images.githubusercontent.com/62292136/83345063-b1d9c300-a349-11ea-9e28-e132529886a1.PNG">
<br/>
<br/>
<img width="607" alt="새계정로그인후_batflat다운로드2" src="https://user-images.githubusercontent.com/62292136/83345064-b30af000-a349-11ea-9261-30f86ff15518.PNG">
<br/>
<br/>
<img width="629" alt="새계정로그인후_batflat다운로드3" src="https://user-images.githubusercontent.com/62292136/83345065-b3a38680-a349-11ea-936d-e099ba30fbb6.PNG">
<br/>
<br/>
<br/>
5) 블로그가 잘 세팅 되었는지 웹브라우저로 확인한다.
<br/>
<br/>
<img width="960" alt="batflat블로그완성" src="https://user-images.githubusercontent.com/62292136/83345071-ccac3780-a349-11ea-995b-cf88a2951f5c.PNG">
<br/>
<br/>
<br/>
## Batflat 관리자 페이지 사용법 정리 ##
<br/>
<br/>
1) 블로그 관리자 페이지 들어가기
<br/>
<br/>
자신이 설정한 도메인 뒤에 /admin 을 붙이면 관리자 페이지로 들어갈 수 있다.
<br/>
<br/>
초기 ID / PW 는 admin 이다.
<br/>
<br/>
<img width="960" alt="블로그관리자페이지" src="https://user-images.githubusercontent.com/62292136/83345075-e6e61580-a349-11ea-8fdf-f22d1f224f76.PNG">
<br/>
<br/>
<br/>
관리자 페이지에 로그인해서 들어가면 이렇게 많은 메뉴들이 있다.
<br/>
<br/>
<img width="960" alt="관리자페이지1" src="https://user-images.githubusercontent.com/62292136/83390135-47e61a00-a42c-11ea-874e-409b9d62ee7d.PNG">
<br/>
<br/>
<br/>
이 중 필요한 몇개의 메뉴의 사용법을 알아보도록 하자.
<br/>
<br/>
<br/>
1) Blog
<br/>
<br/>
가장 기본적인 글을 포스팅하는 곳이다.     
Manage 탭은 현재 포스팅 되어있는 글의 목록을 보여주고,
<br/>
<br/>
<img width="960" alt="관리자페이지_블로그2" src="https://user-images.githubusercontent.com/62292136/83390191-64825200-a42c-11ea-9ffd-297a204ef2ba.PNG">
<br/>
<br/>
<br/>
Add new는 새로운 글을 포스팅할 수 있는 곳이다.
<br/>
<br/>
<img width="960" alt="관리자페이지_블로그" src="https://user-images.githubusercontent.com/62292136/83390186-63512500-a42c-11ea-8caf-956a56c460f0.PNG">
<br/>
<br/>
<br/>
Setting 탭에서는 Blog이름, Description 등을 설정할 수 있다.
<br/>
<br/>
<img width="960" alt="관리자페이지_블로그3" src="https://user-images.githubusercontent.com/62292136/83390195-651ae880-a42c-11ea-97fe-0d9d4cdc99d6.PNG">
<br/>
<br/>
<br/>
2) Navigation
<br/>
<br/>
블로그 우측 상단에 페이지를 전환할 수 있는 버튼의 목록을 만드는 곳이다.
<br/>
<br/>
<img width="960" alt="관리자페이지_네비게이션2" src="https://user-images.githubusercontent.com/62292136/83390354-a57a6680-a42c-11ea-9e66-73fb214eacbc.PNG">
<br/>
<br/>
<br/>
Edit를 눌러서 수정할 수 있다.
<br/>
<br/>
<img width="960" alt="관리자페이지_네비게이션" src="https://user-images.githubusercontent.com/62292136/83390352-a4493980-a42c-11ea-868d-218ad2224e44.PNG">
<br/>
<br/>
<br/>
3) User
<br/>
<br/>
관리 정보를 수정할 수 있는 곳이다.
<br/>
<br/>
<img width="960" alt="관리자페이지_유저2" src="https://user-images.githubusercontent.com/62292136/83390424-c8a51600-a42c-11ea-981c-c0d5991e55a7.PNG">
<br/>
<br/>
<img width="960" alt="관리자페이지_유저" src="https://user-images.githubusercontent.com/62292136/83390422-c773e900-a42c-11ea-9eb7-b842b950abb5.PNG">
<br/>
<br/>
<br/>
4) Settings
<br/>
<br/>
웹사이트 타이틀, Description, 시간, 사용언어, Editor     
등을 수정할 수 있다.
<br/>
<br/>
<img width="960" alt="관리자페이지_세팅" src="https://user-images.githubusercontent.com/62292136/83390530-fab67800-a42c-11ea-8f03-223e701aed6c.PNG">
<br/>
<br/>
<img width="960" alt="관리자페이지_세팅2" src="https://user-images.githubusercontent.com/62292136/83390533-fbe7a500-a42c-11ea-992c-6a07f8c83f4d.PNG">
<br/>
<br/>
<br/>
관리자 페이지에서 내용들을 적절히 변경한 후 잘 적용되었는지 확인한다.
<br/>
<br/>
<img width="960" alt="바뀐블로그" src="https://user-images.githubusercontent.com/62292136/83345232-b4d5b300-a34b-11ea-9d5e-b8c76b806c8b.PNG">
<br/>
<br/>
<br/>
## Github Blog 포스팅 Batflat Blog로 옮기기 ##
<br/>
<br/>
자신의 Github 블로그를 제작하는 Github Repository로 이동한 후 옮기고 싶은 포스팅의 내용을 모두 복사한다.
<br/>
<br/>
<img width="960" alt="블로그글옮기기1" src="https://user-images.githubusercontent.com/62292136/83386287-c25f6b80-a425-11ea-8c1f-0445ae307c0c.PNG">
<br/>
<br/>
<br/>
복사한 후 Batflat 블로그 관리자 페이지 --> Blog탭 --> Add New 탭으로 들어가서      
<br/>
<br/>
<img width="960" alt="블로그글옮기기2" src="https://user-images.githubusercontent.com/62292136/83386290-c3909880-a425-11ea-8420-925873071b35.PNG">
<br/>
<br/>
<br/>
Title에 포스트의 제목, 밑에 빈 칸에 복사했던 포스팅 내용을 붙여넣기 한다.     
Status를 Published로 설정하고 아래에 Enabled Markdown 체크박스를 체크한다.     
Save를 누르면 블로그에 글이 올라간다.
<br/>
<br/>
<img width="960" alt="블로그글옮기기3" src="https://user-images.githubusercontent.com/62292136/83386291-c4292f00-a425-11ea-961f-c4f79fd4e533.PNG">
<br/>
<br/>
<br/>
Blog탭 --> Manage 탭으로 들어가서 포스팅 목록에 올라갔는지 확인한다.
<br/>
<br/>
<img width="960" alt="관리자페이지_블로그2" src="https://user-images.githubusercontent.com/62292136/83386569-3863d280-a426-11ea-90a7-58882ee2b66f.PNG">
<br/>
<br/>
<br/>
마지막으로 다시 블로그에 접속해서 확인한다.     
<br/>
<br/>
<img width="960" alt="블로그글옮기기4" src="https://user-images.githubusercontent.com/62292136/83386295-c4292f00-a425-11ea-94ce-ad512b5f579f.PNG">
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>


