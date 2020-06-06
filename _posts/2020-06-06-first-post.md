---
title: "Server Backup 실습"
date: 2020-06-06 23:05:28 -0000
categories: OSS MariaDB MySQL Server Backup
---







## 라즈베리파이 내의 서버를 일정 기간마다 백업하도록 세팅하는 실습 ##
<br/>
<br/>
<br/>
1) 백업용 디렉토리 생성 후 권한 조정
<br/>
<br/>
라즈베리파이의 관리자계정으로 로그인한 후 sudo su - 명령을 통해 슈퍼유저가 된다.
<br/>
백업용 디렉토리를 생성하고 권한을 변경한다.
<br/>
<br/>
<br/>
2) 백업 스크립트 작성
<br/>
<br/>
backup.sh 파일을 root디렉토리 내에 생성하고 권한을 변경한다.
<br/>
<br/>
backup.sh 파일을 작성한다.
<br/>
<br/>
백업스크립트가 잘 작성되었는지 확인하기 위해서 실행한다.
<br/>
<br/>
<br/>
3) 백업 스크립트 자동 실행 등록
<br/>
<br/>
<br/>
crontab -e 명령어를 입력한 후 2번 vim 을 선택해서 파일을 작성한다.
<br/>
<br/>
마지막 줄에 백업을 실행할 주기를 정해서 입력한다.
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
