---
title: "Linux 주요 커맨드 - 9. Permissions"
date: 2020-03-22 21:47:28 -0000
categories: Linux OSS
---

## 1. id       
현재 사용자의 실제 id, 유효한 id, 그룹 id 출력           
사용방법 : id     
![id](https://user-images.githubusercontent.com/62292136/77249780-dd279e00-6c86-11ea-92f2-ae6b14fc1faf.PNG)     
     
     
    
## 2. chmod
파일 및 디렉토리의 권한을 변경해줌     
예) -rw-rw-r-- ----------> 앞의 -는 파일의 종류를 표시 (- : 일반 파일, d : 디렉토리, l : smybolic link)     
앞의 문자 하나 이후로 3자리씩 끊어서 소용자 / 그룹 / 일반 사용자 의 권한으로 나뉜다.     
     
권한 : 0 ---> -                    (r: 읽기, w: 읽기, x: 실행)     
       1 ---> x     
       2 ---> w     
       3 ---> wx     
       4 ---> r     
       5 ---> rx     
       6 ---> rw     
       7 ---> rwx     
사용방법 : chmod [변경권한(숫자로표시)] [파일명 혹은 디렉토리명]          
![chmod](https://user-images.githubusercontent.com/62292136/77249927-df3e2c80-6c87-11ea-9149-2672eddd0219.PNG)     
     
     
     
## 3. umask
파일이나 디렉토리의 권한부여 기본값 설정          
사용방법 : umask [부여할 권한 기본값(숫자로 표시)]          
![umask](https://user-images.githubusercontent.com/62292136/77249955-0bf24400-6c88-11ea-995c-1425853387b5.PNG)     

