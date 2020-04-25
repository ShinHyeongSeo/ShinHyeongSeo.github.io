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
현재 작업하고 있는 branch에 다른 branch를 통합한다.     
이 명령을 사용할 때는 현재 위치하고 있는 branch를 주의해야한다.     
사용 방법 : git merge [병합할 branch명]     
     
     
     
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
1. rebase -i --root 입력
<img width="482" alt="rebase" src="https://user-images.githubusercontent.com/62292136/80284819-cc71b880-875b-11ea-8f8e-2f495164580e.PNG">      
     
2. commit message를 수정할 commit의 pick을 reword로 교체
<img width="481" alt="rebase_1" src="https://user-images.githubusercontent.com/62292136/80284820-cd0a4f00-875b-11ea-8477-c6dbbce2a41e.PNG">
<img width="483" alt="rebase_2" src="https://user-images.githubusercontent.com/62292136/80284821-cda2e580-875b-11ea-92ee-0a2a3247e40f.PNG">     
     
3. commit message를 수정한 후 저장
<img width="480" alt="rebase_3" src="https://user-images.githubusercontent.com/62292136/80284822-ce3b7c00-875b-11ea-9996-f984b0f87a9f.PNG">
<img width="481" alt="rebase_4" src="https://user-images.githubusercontent.com/62292136/80284824-ce3b7c00-875b-11ea-8d6a-993e25269398.PNG">     
     
4. git log로 변경된 사항 확인
<img width="481" alt="rebase_5" src="https://user-images.githubusercontent.com/62292136/80284826-ced41280-875b-11ea-8d1f-7170f1343b74.PNG">     
     
          
     
     
     
     
     
# 2. 실습 예제     
이와 같은 순서로 commit, merge를 통해 Local Repository에 적용
<img width="743" alt="캡처" src="https://user-images.githubusercontent.com/62292136/80284352-09887b80-8759-11ea-8255-2b5acbbdc8ea.PNG">     
     
     
     
     
     
### 1.      
### 2.      
### 3.      
### 4.      
### 5.     
### 6. 
### 7.      
### 8. 
### 9. 
### 10.
### 11. 
