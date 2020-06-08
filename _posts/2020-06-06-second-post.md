---
title: "Wordpress 설치 실습"
date: 2020-06-06 23:13:28 -0000
categories: OSS MariaDB MySQL Server WordPress Raspberrypi
---







## 라즈베리파이 DB 내에 Wordpress 설치하는 실습 ##
<br/>
<br/>
<br/>
1) 설치파일 다운로드 및 압축 풀기
<br/>
<br/>
Wordpress를 설치해서 사용할 계정으로 로그인 한 후, html 디렉토리로 이동한다.       
wget https://ko.wordpress.org/latest-ko_KR.tar.gz 명령어를 통해 설치파일을 다운로드 하고       
tar -xzvf latest-ko_KR.tar.gz 명령어를 통해 압축 풀기를 실행 한다.
<br/>
<br/>
<img width="852" alt="wordpress설치1" src="https://user-images.githubusercontent.com/62292136/84025681-fbb84e00-a9c6-11ea-8299-2374fdf76ae5.PNG">
<br/>
<br/>
<br/>
2) 설치 페이지 실행
<br/>
<br/>
자신이 세팅했던 도메인 주소/wordpress 를 주소창에 입력해 wordpress 설치페이지로 접속한다.
<br/>
<br/>
<img width="960" alt="wordpress접속1" src="https://user-images.githubusercontent.com/62292136/84025765-17bbef80-a9c7-11ea-94a2-9fb9088c5702.PNG">
<br/>
<br/>
<br/>
3) DB 연결정보 입력
<br/>
<br/>
사용자용 DB, DB 사용자계정, 비밀번호를 입력한다.
<br/>
<br/>
<img width="960" alt="wordpress접속2" src="https://user-images.githubusercontent.com/62292136/84025851-3621eb00-a9c7-11ea-9dab-0e0219787e08.PNG">
<br/>
<br/>
<br/>
4) wp-config.php 파일 제작
<br/>
<br/>
다음으로 넘어갔을 때 wp-config.php 파일을 자동으로 만들 수 없다고 뜬다.
<br/>
<img width="960" alt="wordpress접속3" src="https://user-images.githubusercontent.com/62292136/84025874-3e7a2600-a9c7-11ea-8955-f62cc57c6d63.PNG">
<br/>
<br/>
따라서 html 디렉토리 내에 wp-config.php 파일을 수동으로 생성하여       
사이트에 있는 내용을 복사하여 붙여넣는다.
<br/>
<img width="960" alt="wp-config php파일작성" src="https://user-images.githubusercontent.com/62292136/84026015-7e410d80-a9c7-11ea-9a17-882c161fdb7c.PNG">
<br/>
<br/>
<br/>
5) 사이트 제목, 관리자 정보 입력
<br/>
<br/>
위에서 wp-config.php 파일을 작성하고 나서 사이트를 접속하면     
성공적으로 접속된 것을 확인할 수 있다.
<br/>
<br/>
<img width="960" alt="wordpress접속4" src="https://user-images.githubusercontent.com/62292136/84026266-f6a7ce80-a9c7-11ea-9494-152d0741fd90.PNG">
<br/>
<br/>
사이트 제목과 관리자 정보를 입력하면 된다.
<br/>
<br/>
<br/>
6) 설치 완료 후 로그인 후 들어가기
<br/>
<br/>
성공적으로 설치된 것을 확인한 후에
<br/>
<br/>
<img width="960" alt="wordpress접속5" src="https://user-images.githubusercontent.com/62292136/84026324-19d27e00-a9c8-11ea-923b-5c8cf4fe8978.PNG">
<br/>
<br/>
로그인을 해서 관리자 페이지로 들어가서 확인한다.
<br/>
<br/>
<img width="960" alt="wordpress로그인완료" src="https://user-images.githubusercontent.com/62292136/84026409-3ec6f100-a9c8-11ea-8596-8730e052022b.PNG">
<br/>
<br/>
<br/>
## Wordpress 관리용 테마 설정 방법 ##
<br/>
<br/>
<br/>
1) Wordpress 관리를 위해 디렉토리 권한 변경
<br/>
<br/>
사용자 계정으로 로그인 후,      
sudo chgrp -R www-data ~/html/wordpress/wp-content       
sudo chmod -R 775 ~html/wordpress/wp-content     
명령어들을 통해 디렉토리의 권한을 변경한다.
<br/>
<br/>
* 만약 sudo가 실행이 안된다면 구글링을 통해 sudoer 파일을 수정방법을 찾아보도록 하자!
<br/>
<br/>
2) wp-config.php 파일 수정 
<br/>
<br/>
관리자 페이지에서 테마를 직접 설치할 수 있도록 파일의 내용을 수정한다.
<br/>
<br/>
wp-config.php 파일 마지막에 define('FS_METHOD', 'direct'); 명령 한줄을 추가한다.
<br/>
<br/>
3) wordpress 원하는 테마 다운로드 및 활성화
<br/>
<br/>
<br/>
<br/>
