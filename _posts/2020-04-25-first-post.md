---
title: "Git 명령어 정리2"
date: 2020-04-25 23:36:28 -0000
categories: Linux OSS Git cowork
---
     
     
     
# 1. Git 명령어 정리

## 1. 작업 공간 관련 명령어
### 1. branch
새로운 branch를 만들거나 현재 어느 branch에서 작업하고 있는지 알려준다.            
사용 방법 : git branch [branch명] / git branch     
     
     
     
### 2. merge
현재 작업하고 있는 branch에 다른 branch를 통합시킨다.     
이 명령을 사용할 때는 현재 위치하고 있는 branch를 주의해야한다.     
사용 방법 : git merge [통합할 branch명]     
     
     
     
### 3. checkout
작업하고 있는 branch를 변경할 때 사용한다.          
사용 방법 : git checkout [이동할 branch명]          
     
     
     
     
     
     
     
     
## 2. 파일 상태 관련 명령어
### 1. revert
특정 시점의 commit으로 돌아가고 싶을 때 그 commit으로 되돌아가는 commit을 추가로 수행한다.    
사용 방법 : git revert HEAD / git revert [돌아갈 commit의 checksum]     
     
     
     
현재 commit log 확인 후 git revert HEAD를 통해 가장 최근의 commit으로 되돌림     
<img width="480" alt="revert" src="https://user-images.githubusercontent.com/62292136/80284594-7a7c6300-875a-11ea-9a0c-261bed2b33ca.PNG">      
     
commit message 생성, 기본값은 "Revert '마지막commit message'"로 되어있음, 변경 가능     
<img width="483" alt="revert_1" src="https://user-images.githubusercontent.com/62292136/80284596-7bad9000-875a-11ea-9887-04b9dc7354c3.PNG">     
     
commit log 기록을 통해 commit이 되돌아 간 것을 확인     
<img width="484" alt="revert_2" src="https://user-images.githubusercontent.com/62292136/80284597-7c462680-875a-11ea-90a9-9b0604d22f1e.PNG">     
     
파일의 내용 또한 변경되어있음     
<img width="483" alt="revert_3" src="https://user-images.githubusercontent.com/62292136/80284599-7c462680-875a-11ea-96df-7e5b9f46b319.PNG">     
     
     
     
     
     
     
### 2. reset
특정 시점의 commit으로 돌아가고 싶을 때 commit 자체를 과거로 되돌리고 문제된 commit을 삭제한다.          
사용 방법 : git reset [돌아갈 commit의 checksum]          
     
     
     
     
되돌아가고 싶은 commit의 checksum 입력     
<img width="481" alt="reset" src="https://user-images.githubusercontent.com/62292136/80284701-11491f80-875b-11ea-8e64-4751de857a17.PNG">     
   
commit log 기록을 통해 commit이 되돌아 간 것을 확인     
<img width="482" alt="reset_1" src="https://user-images.githubusercontent.com/62292136/80284702-11e1b600-875b-11ea-8631-26dfb525c6de.PNG">     
     
파일의 내용은 바뀌지 않음     
<img width="484" alt="reset_2" src="https://user-images.githubusercontent.com/62292136/80284703-127a4c80-875b-11ea-9b01-139e4a663523.PNG">     
     
     
     
     

### 3. rebase   
예전 commit의 commit message를 바꿀 때 사용한다.     
잠시 commit들의 base를 과거로 바꾼 다음 commit message를 수정한다.     
     
사용 방법     
rebase -i --root 입력     
<img width="482" alt="rebase" src="https://user-images.githubusercontent.com/62292136/80284819-cc71b880-875b-11ea-8f8e-2f495164580e.PNG">      
     
commit message를 수정할 commit의 pick을 reword로 교체     
<img width="481" alt="rebase_1" src="https://user-images.githubusercontent.com/62292136/80284820-cd0a4f00-875b-11ea-8477-c6dbbce2a41e.PNG">     
     
<img width="483" alt="rebase_2" src="https://user-images.githubusercontent.com/62292136/80284821-cda2e580-875b-11ea-92ee-0a2a3247e40f.PNG">     
     
commit message를 수정한 후 저장     
<img width="480" alt="rebase_3" src="https://user-images.githubusercontent.com/62292136/80284822-ce3b7c00-875b-11ea-9996-f984b0f87a9f.PNG">     
     
<img width="481" alt="rebase_4" src="https://user-images.githubusercontent.com/62292136/80284824-ce3b7c00-875b-11ea-8d6a-993e25269398.PNG">     
     
git log로 변경된 사항 확인     
<img width="481" alt="rebase_5" src="https://user-images.githubusercontent.com/62292136/80284826-ced41280-875b-11ea-8d1f-7170f1343b74.PNG">     
     
          
     
     
     
     
     
# 2. 실습 예제     
이와 같은 순서로 commit, merge를 통해 Local Repository에 적용
<img width="743" alt="캡처" src="https://user-images.githubusercontent.com/62292136/80284352-09887b80-8759-11ea-8255-2b5acbbdc8ea.PNG">     
     
     
     
     
     
### 1. Version1
현재 디렉토리에 새로운 git repository를 생성하고     
my.txt 파일을 만든 후 add commit을 통해 Version 1을 git repository에 등록한다.          
<img width="482" alt="Version1" src="https://user-images.githubusercontent.com/62292136/80285015-1c9d4a80-875d-11ea-95b3-111c64b7294b.PNG">     
     
### 2. Version2
my.txt 내용 수정 후 add commit을 통해 Version 2를 git repository에 등록한다.          
<img width="484" alt="Version2" src="https://user-images.githubusercontent.com/62292136/80285017-1d35e100-875d-11ea-9205-f7f7efcb005d.PNG">     
     
<img width="482" alt="Version2_1" src="https://user-images.githubusercontent.com/62292136/80285018-1dce7780-875d-11ea-9094-8e9bac5010f7.PNG">     
     
### 3. Version3
my.txt 내용 수정 후 add commit을 통해 Version3를 git repository에 등록한다.          
<img width="484" alt="Version3" src="https://user-images.githubusercontent.com/62292136/80285020-1e670e00-875d-11ea-9c6f-7068cc2abdb5.PNG">     
     
<img width="482" alt="Version3_1" src="https://user-images.githubusercontent.com/62292136/80285022-1e670e00-875d-11ea-822d-a103589827ce.PNG">     
     
### 4. Version4
새로운 branch second를 생성하고 작업공간을 이동한 후     
my.txt 내용 수정 후 add commit을 통해 Version4를 git repository에 등록한다.   
<img width="481" alt="Version4" src="https://user-images.githubusercontent.com/62292136/80285023-1effa480-875d-11ea-9809-3869c9ce0324.PNG">     
     
<img width="482" alt="Version4_2" src="https://user-images.githubusercontent.com/62292136/80285026-1f983b00-875d-11ea-98b1-f0a1aadf2ded.PNG">     
     
<img width="478" alt="Version4_1" src="https://user-images.githubusercontent.com/62292136/80285025-1effa480-875d-11ea-9f98-7e3d4a5f5833.PNG">     
     
### 5. Version5
master branch로 작업공간을 이동한 후     
my.txt 내용 수정 후 add commit을 통해 Version5를 git repository에 등록한다.     
<img width="483" alt="Version5" src="https://user-images.githubusercontent.com/62292136/80285027-2030d180-875d-11ea-9b56-75fd2ce145e7.PNG">     
     
<img width="482" alt="Version5_1" src="https://user-images.githubusercontent.com/62292136/80285029-2030d180-875d-11ea-960e-029357519a09.PNG">     
     
<img width="483" alt="Version5_2" src="https://user-images.githubusercontent.com/62292136/80285030-20c96800-875d-11ea-8f57-36c72249ee3a.PNG">     
     
     
### 6. Version6
my.txt 내용 수정 후 add commit을 통해 Version 6를 git repository에 등록한다.     
<img width="481" alt="Version6" src="https://user-images.githubusercontent.com/62292136/80285031-2161fe80-875d-11ea-9413-0785c47011ff.PNG">     
     
<img width="483" alt="Version6_1" src="https://user-images.githubusercontent.com/62292136/80285032-2161fe80-875d-11ea-92a6-966ecc1c767a.PNG">     
     
     
### 7. Version7
second branch로 작업공간을 이동한 후     
my.txt 내용 수정 후 add commit을 통해 Version7을 git repository에 등록한다.     
<img width="481" alt="Version7" src="https://user-images.githubusercontent.com/62292136/80285034-21fa9500-875d-11ea-8fa8-618c3ff75cc5.PNG">     
     
<img width="481" alt="Version7_1" src="https://user-images.githubusercontent.com/62292136/80285035-21fa9500-875d-11ea-8bcb-5f83d5e48719.PNG">     
     
<img width="481" alt="Version7_2" src="https://user-images.githubusercontent.com/62292136/80285037-22932b80-875d-11ea-92a8-0aa23e706948.PNG">     
     
### 8. Version8
master branch로 작업공간을 이동한 후     
second branch를 master branch에 통합시킨 후     
add commit을 통해 Version8을 git repository에 등록한다.         
     
동시에 양쪽의 branch에서 똑같은 파일이 수정되어서 conflict가 발생한다.     
<img width="481" alt="Version8" src="https://user-images.githubusercontent.com/62292136/80285038-232bc200-875d-11ea-9cf8-aa6f26ac9a9d.PNG">      
     
<img width="479" alt="Version8_1" src="https://user-images.githubusercontent.com/62292136/80285039-232bc200-875d-11ea-9766-2c731481fede.PNG">     
     
그래서 수동으로 my.txt의 내용 수정 후     
<img width="483" alt="Version8_2" src="https://user-images.githubusercontent.com/62292136/80285040-23c45880-875d-11ea-941b-3a9573669b7a.PNG">     
     
<img width="482" alt="Version8_3" src="https://user-images.githubusercontent.com/62292136/80285041-23c45880-875d-11ea-8e8a-2076dbf688fd.PNG">     
     
add commit을 통해 Version 8을 git repository에 등록한다.     
<img width="479" alt="Version8_4" src="https://user-images.githubusercontent.com/62292136/80285042-245cef00-875d-11ea-9244-b788f39b43c5.PNG">     
     
### 9. Version9
my.txt 내용 수정 후 add commit을 통해 Version 9를 git repository에 등록한다.     
<img width="481" alt="Version9" src="https://user-images.githubusercontent.com/62292136/80285043-24f58580-875d-11ea-9fc2-fa4aa4b787ab.PNG">     
      
<img width="480" alt="Version9_1" src="https://user-images.githubusercontent.com/62292136/80285044-24f58580-875d-11ea-89af-8fb97a2a8823.PNG">     
    
     
     
