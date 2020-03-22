---
title: "Linux 주요 커맨드 - 6. Redirection"
date: 2020-03-22 20:22:28 -0000
categories: Linux OSS
---

## 1. sort       
파일의 내용을 오름차순으로 정렬           
사용방법 : type [파일명]     
![sort](https://user-images.githubusercontent.com/62292136/77249369-e95e2c00-6c83-11ea-8b73-7d1e135c87b9.PNG)     
     
     
    
## 2. uniq     
파일의 내용중에서 중복된 내용의 행이 연속으로 있으면 하나만 남기고 삭제          
사용방법 : uniq [파일명]     
![uniq](https://user-images.githubusercontent.com/62292136/77249391-1ca0bb00-6c84-11ea-9ff5-00820ad56c4d.PNG)     
     
     
     
     
## 3. grep     
파일에서 특정 문자열을 찾아서 화면에 표시해줌     
대소문자 구별하고, 결과값은 빨간 글씨로 출력     
사용방법 : grep [찾을 문자열] [파일명]          
![grep](https://user-images.githubusercontent.com/62292136/77249437-5b367580-6c84-11ea-8660-9413a9d9ae33.PNG)     
     
     
     
## 4. wc     
파일의 줄 수, 단어 수, 글자 수를 화면에 표시해줌     
뒤에 -l 을 붙이면 줄 수만     
뒤에 -w 를 붙이면 단어 수만     
뒤에 -c 를 붙이면 글자 수만 출력 가능     
사용방법 : wc [파일명]              
![wc](https://user-images.githubusercontent.com/62292136/77249484-a5b7f200-6c84-11ea-8e32-92e027e5e8cd.PNG)     
     
     
     
## 5. head          
파일 내용 중 상위 10줄을 출력     
뒤에 -숫자 붙일 시 숫자만큼의 줄을 출력     
사용방법 : head [파일명]     
![head](https://user-images.githubusercontent.com/62292136/77249517-e7e13380-6c84-11ea-8004-bbcc89a5ae0b.PNG)     
     
     
     
## 6. tail     
파일 내용 중 하위 10줄을 출력     
뒤에 -숫자 붙일 시 숫자만큼의 줄을 출력     
사용방법 : tail [파일명]     
![tail](https://user-images.githubusercontent.com/62292136/77249536-09dab600-6c85-11ea-9910-217b6f8ae8d2.PNG)     
     
     
     
## 7. tee         
결과 화면을 새로운 파일로 저장          
사용방법 : cat [파일명] | tee [새로운 파일명]          
![tee](https://user-images.githubusercontent.com/62292136/77249557-41496280-6c85-11ea-9419-4e7f7233516c.PNG)     
