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
5) 블로그가 잘 세팅 되었는지 웹브라우저로 확인한다.
<br/>
<br/>
<br/>
6) 블로그 관리자 페이지 들어가보기
<br/>
<br/>
자신이 설정한 도메인 뒤에 /admin 을 붙이면 관리자 페이지로 들어갈 수 있다.
<br/>
<br/>
초기 ID / PW 는 admin 이다.
<br/>
<br/>
<br/>
7) 관리자 페이지에서 내용들을 적절히 변경한 후 잘 적용되었는지 확인한다.
<br/>
<br/>
<br/>
8) 이때까지 Github Blog 에서 관리하던 글들을 Batflat 블로그에 옮겨서 포스팅한다.
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
