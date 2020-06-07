---
title: "DB Engine 설치"
date: 2020-06-03 00:36:28 -0000
categories: OSS MariaDB Hosting nginx
---












## DB Engine 설치 실습 ##
1) MariaDB / MySQL 설치
<br/>
<br/>
관리자 계정으로 로그인 한 후, sudo su - 명령어를 통해 슈퍼유저가 된다.
<br/>
<br/>
<img width="606" alt="슈퍼유저되기" src="https://user-images.githubusercontent.com/62292136/83959994-9e38da00-a8be-11ea-9f61-4058759f0664.PNG">
<br/>
<br/>
apt-get-y install mariadb-server 명령어를 통해 MariaDB를 설치한다.
<br/>
<br/>
<img width="673" alt="mariadb설치" src="https://user-images.githubusercontent.com/62292136/83959995-a42ebb00-a8be-11ea-8f1b-27a27fb1f5f7.PNG">
<br/>
<br/>
cd /etc/mysql/mariadb.conf.d 명령어를 통해 해당 디렉토리로 이동한다.
<br/>
<br/>
<img width="647" alt="cnf목록들" src="https://user-images.githubusercontent.com/62292136/83960094-a7767680-a8bf-11ea-9c98-b96727b3dd8a.PNG">
<br/>
<br/>
50-server.cnf 파일의 내용을 한국어 사용을 위해 알맞게 수정한다.
<br/>
<br/>
<img width="332" alt="server conf변경전" src="https://user-images.githubusercontent.com/62292136/83960037-2c14c500-a8bf-11ea-8566-9aec93bb49c4.PNG">
<br/>
<br/>
<img width="405" alt="server conf변경후" src="https://user-images.githubusercontent.com/62292136/83960038-2cad5b80-a8bf-11ea-9194-e432419bbf16.PNG">
<br/>
<br/>
50-client.cnf 파일의 내용 역시 수정한다. 
<br/>
<br/>
<img width="583" alt="client conf변경전" src="https://user-images.githubusercontent.com/62292136/83960049-4353b280-a8bf-11ea-8881-c460f51471f2.PNG">
<br/>
<br/>
<img width="565" alt="client conf변경후" src="https://user-images.githubusercontent.com/62292136/83960050-43ec4900-a8bf-11ea-9df3-0446fb483a3b.PNG">
<br/>
<br/>
apt install php-mysql 명령어를 통해 이번에는 MySQL을 설치한다.
<br/>
<br/>
<img width="730" alt="php_mysql설치" src="https://user-images.githubusercontent.com/62292136/83960095-aa716700-a8bf-11ea-8111-9ab46132da96.PNG">
<br/>
<br/>
service mysql restart 명령어를 통해 서버를 재시작한다.
<br/>
<br/>
설치된 mariadb의 root 비밀번호를 생성한다.
<br/>
<br/>
<img width="680" alt="mariadb비밀번호생성" src="https://user-images.githubusercontent.com/62292136/83960108-ce34ad00-a8bf-11ea-9788-8829a5e587f5.PNG">
<br/>
<br/>
<br/>
2) 특정 사용자 위한 DB 생성
<br/>
<br/>
3) 서버관리자에게 웹서비스 세팅 확인 요청
<br/>
<br/>
4) PHP+MySQL 사용하는 웹사이트 소스 git clone
<br/>
<br/>
5) 서버관리자로부터 받은 DB 정보 반영
<br/>
<br/>
6) 사용자 DB에 테이블 생성
<br/>
<br/>
7) 웹사이트 접속 테스트
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

