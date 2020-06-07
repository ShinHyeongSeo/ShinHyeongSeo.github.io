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
<br/>
백업용 디렉토리를 생성하고 권한을 변경한다.
<br/>
<br/>
<img width="612" alt="백업용디렉토리생성_권한변경" src="https://user-images.githubusercontent.com/62292136/83961391-a3515580-a8cd-11ea-8272-c46195262477.PNG">
<br/>
<br/>
<br/>
2) 백업 스크립트 작성
<br/>
<br/>
backup.sh 파일을 root디렉토리 내에 생성하고 권한을 변경한다.
<br/>
<br/>
<img width="565" alt="백업스크립트테스트3" src="https://user-images.githubusercontent.com/62292136/83961477-6afe4700-a8ce-11ea-86af-3db7ea2fbb6e.PNG">
<br/>
<br/>
backup.sh 파일을 작성한다.
<br/>
<br/>
<img width="726" alt="백업스크립트작성" src="https://user-images.githubusercontent.com/62292136/83961470-4e620f00-a8ce-11ea-99e3-4567eced3fda.PNG">
<br/>
<br/>
첫번 째 줄부터 차례로,     
사용자 데이터를 압축백업하는 명령      
사용자 DB를 백업하는 명령      
일주일 지난 백업파일 삭제하는 명령이다.
<br/>
<br/>
./backup.sh 명령어를 통해 백업스크립트를 실행한다.
<br/>
<br/>
백업스크립트가 잘 생성되었는지 목록을 확인한다.
<br/>
<br/>
<img width="564" alt="백업스크립트테스트2" src="https://user-images.githubusercontent.com/62292136/83961450-1955bc80-a8ce-11ea-8aa0-10d09b5dd617.PNG">
<br/>
<br/>
<br/>
3) 백업 스크립트 자동 실행 등록
<br/>
<br/>
서버 백업을 관리자가 직접 하기에는 너무 번거로운 행동이다.
<br/>
<br/>
따라서 서버 자체에서 주기에 따라 자동으로 백업을 하도록 설정을 해보겠다.
<br/>
<br/>
crontab -e 명령어를 입력한 후 2번 vim 을 선택해서 파일을 작성한다.
<br/>
<br/>
<img width="549" alt="백업스크립트자동실행등록_0" src="https://user-images.githubusercontent.com/62292136/83961550-4787cc00-a8cf-11ea-93b6-da77f69addc3.PNG">
<br/>
<br/>
마지막 줄에 백업을 실행할 주기를 정해서 입력한다.
<br/>
<br/>
<img width="621" alt="백업스크립트자동실행등록" src="https://user-images.githubusercontent.com/62292136/83961549-45be0880-a8cf-11ea-912d-1e9333d6e298.PNG">
<br/>
<br/>
<br/>
첫번째 * 부터 분, 시, 일, 월, 주 단위이다.        
본인은 매일 오전 4시에 자동으로 백업하도록 설정하였다.
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
