---
title: "Git 명령어 정리"
date: 2020-04-11 17:49:28 -0000
categories: Linux OSS Git
---
# 1. Git 작업 구조의 이해
### 1. Working Directory
Working Directory란 현재 우리가 파일을 작업하고 있는 공간이다.
### 2. Staging Area
Staging Area는 Working Directory에서 작업한 파일들이 add가 되서 저장되는 공간이다.
### 3. Local Repository
Local Repository는 Staging Area에 저장된 파일들을 commit하면 저장되는 공간이다.
### 4. Remote Repository
Remote Repository는 Local Repository에 저장된 파일들이 push되어서 저장되는 Github사이트나 원격 저장소 같은 공간이다.     
     
     
     
     
     
     
     
     
     
# 2. Git 명령어 정리
## 1. 작업 공간 시작

### 1. init
로컬 저장소로 사용할 폴더를 생성하여 해당 폴더로 이동 후 "git init"을 입력하면 새로운 git저장소가 만들어진다.    
(지금 있는 디렉토리를 git을 통해 버전관리를 하겠다고 지정함)   
사용 방법 : git init     
     
     
     
### 2. clone
기존에 다른곳에 있던 저장소를 복사해서 새 디렉토리로 가져온다.     
(다른 프로젝트에 참여할때 자주 사용)     
사용 방법     
git clone /로컬/저장소/경로                      -----> 로컬 저장소 복제          
git clone 사용자명@호스트:/원격/저장소/경로       -----> 원격 서버의 저장소 복제          
    
     
     
## 2. 변경 사항에 대한 작업
### 1. add
파일을 staging area에 추가하거나 원격 저장소를 추가할 때 사용한다.     
사용 방법     
git add                       -----> 소스파일들을 staging area에 추가       
git remote add origin <url>   -----> 로컬 저장소에 있는 파일들을 등록할 원격 저장소를 추가     
     
     
     
### 2. mv
파일의 이름을 변경할 때 쓰인다.     
사용 방법 : git mv <기존 파일명> <바꿀 파일명>     
<img width="483" alt="git_mv" src="https://user-images.githubusercontent.com/62292136/79073002-0637cd80-7d1f-11ea-8ff3-00991b475852.PNG">
     
     
     
     
### 3. reset
파일의 add를 취소하고 staged됐던 파일들은 unstaged 상태로 되돌린다.     
사용 방법 : git reset <파일명>     
<img width="394" alt="reset_1" src="https://user-images.githubusercontent.com/62292136/79073023-1f407e80-7d1f-11ea-8e3c-c84ca08cd13c.PNG">     
     
<img width="517" alt="reset_2" src="https://user-images.githubusercontent.com/62292136/79073027-22d40580-7d1f-11ea-95b3-9276c055e843.PNG">     
     
     
     
     
### 4. rm     
git과 로컬 디렉토리에서 파일을 모두 삭제할 때 쓰인다.     
사용 방법     
git rm <파일명>   ---> remote repository와 로컬 디렉토리에서 파일을 모두 삭제한다.       
<img width="583" alt="rm_1" src="https://user-images.githubusercontent.com/62292136/79073048-45661e80-7d1f-11ea-9486-6a1cf01f5a8a.PNG">     
     
<img width="945" alt="rm_2" src="https://user-images.githubusercontent.com/62292136/79073049-47c87880-7d1f-11ea-9a9b-2e7d709127a9.PNG">     
     
git rm --cached <파일명> ---> remote repository에 있는 파일만 삭제하고 로컬 디렉토리에서 파일은 삭제하지 않는다.     
<img width="946" alt="rm--cached" src="https://user-images.githubusercontent.com/62292136/79073086-80685200-7d1f-11ea-9d06-34b54b0e0c2c.PNG">     
<img width="645" alt="git_rm-cached3" src="https://user-images.githubusercontent.com/62292136/79073088-82caac00-7d1f-11ea-90e5-0df0ac76db5c.PNG">     
<img width="610" alt="git_rm_cached4" src="https://user-images.githubusercontent.com/62292136/79073090-85c59c80-7d1f-11ea-98e0-aa79890c8a34.PNG">     
<img width="944" alt="rm_--cached2" src="https://user-images.githubusercontent.com/62292136/79073096-8f4f0480-7d1f-11ea-8132-93b3391d8619.PNG">     
     
     
     
## 3. 커밋 내역 표시 및 조작     
### 1. commit
staging area에 파일들을 local repository에 등록할 때 쓰인다.     
사용 방법     
git commit -m "comment"     ----> -m "comment" 를 입력하면 commit할때 어떤 점이 변경되었는지 알수 있게 comment를 표시해준다.     
     
     
     
### 2. checkout
working directory에서 수정한 파일내용을 가장 최근의 commit한 파일내용으로 되돌리고 싶을 때 사용한다.     
사용 방법 : git checkout <파일명>     
<img width="582" alt="checkout" src="https://user-images.githubusercontent.com/62292136/79073126-bc031c00-7d1f-11ea-813a-bc2e7eb48f12.PNG">     
     
     
     
### 3. diff
working directory에서 작업한 파일의 내용과 staging area에 있는 파일내용의 차이점을 보여줄 때 쓰인다.     
git --oneline 을 통해 얻은 이때까지 commit했던 checksum값을 알아내서 commit했던 내용간의 차이점을 보여줄 때 쓰인다.     
staging area에 있는 파일과 최근에 commit했던 파일들의 차이점을 보여줄 때 쓰인다.     
     
사용 방법
git diff                           -----> working directory에서 작업한 파일의 내용과 가장 최근에 commit한 파일내용의 차이점을 보여줌     
<img width="296" alt="git_diff" src="https://user-images.githubusercontent.com/62292136/79073195-287e1b00-7d20-11ea-9e37-948e2ec8c99b.PNG">     
     
git diff <checksum1> <checksum2>   -----> 이때까지 commit했던 내용들의 checksum을 입력해 내용간의 차이점을 보여줌     
<img width="625" alt="git_diff_2개" src="https://user-images.githubusercontent.com/62292136/79073217-4b103400-7d20-11ea-8a80-23f2d4ee8848.PNG">     
     
<img width="945" height = "400" alt="git_diff_2r개_결과" src="https://user-images.githubusercontent.com/62292136/79073219-4e0b2480-7d20-11ea-88fb-2e5b5f8a5413.PNG">     
     
git diff --staged                  -----> staging area에 있는 파일내용과 commit했던 파일내용의 차이점을 보여줌     
<img width="593" height = "300" alt="git_diff_staged" src="https://user-images.githubusercontent.com/62292136/79073256-7dba2c80-7d20-11ea-8f01-4308e78419c3.PNG">     
     
<img width="595" height = "300" alt="git_diff_staged2" src="https://user-images.githubusercontent.com/62292136/79073257-7f83f000-7d20-11ea-8465-206a8ab8a008.PNG">     
     
     
     
     
## 4. 커밋 내역 및 상태보기     
### 1. log
이때까지 commit했던 기록들을 보여준다.     
사용 방법     
git log ---> 이때까지 commit했던 기록들을 보여줌     
<img width="481" alt="git_log" src="https://user-images.githubusercontent.com/62292136/79073370-22d50500-7d21-11ea-9b3e-35d9d6b0c659.PNG">     
     
git log --oneline ---> 이때까지 commit했던 기록들을 각각 한 줄로 보여줌 (check sum 7자리까지만)   
<img width="481" alt="gitlog_oneline" src="https://user-images.githubusercontent.com/62292136/79073383-32ece480-7d21-11ea-80fd-dbb395f1c5a1.PNG">     
     
git log --pretty=oneline ---> 이때까지 commit했던 기록들을 각각 한줄로 보여줌 check sum 전체)     
<img width="484" alt="git_log--pretty=oneline" src="https://user-images.githubusercontent.com/62292136/79073386-35e7d500-7d21-11ea-8cac-4e261371a381.PNG">     
     
git log --graph ---> 이때까지 commit했던 기록들을 그래프 형식으로 보여줌     
<img width="484" alt="git_log--graph" src="https://user-images.githubusercontent.com/62292136/79073391-3da77980-7d21-11ea-833d-d88590b78a6e.PNG">     
     
git log -p -1 ---> 가장 최근의 commit했던 파일의 내용 중 변경된 내용을 보여줌     
<img width="481" alt="git_log-p-1" src="https://user-images.githubusercontent.com/62292136/79073396-40a26a00-7d21-11ea-9700-6e651c3c237a.PNG">     
     
     
     
     
### 2. status
working directory의 상태를 표시해준다.     
사용 방법     
git status ---> working directory 상태 표시해줌     
<img width="595" alt="git_status" src="https://user-images.githubusercontent.com/62292136/79073427-79dada00-7d21-11ea-892c-a15628442562.PNG">     
     
git status -s ---> working directory 상태 한 줄로 간단히 표시해줌     
<img width="594" alt="git_status -s" src="https://user-images.githubusercontent.com/62292136/79073429-7b0c0700-7d21-11ea-94d6-ea4d8216ed25.PNG">     
     
     
     
### 3. show
가장 최근의 commit기록 중 파일의 내용의 차이점을 보여줄 때 쓰인다.          
사용 방법 : git show     
<img width="591" alt="git_show" src="https://user-images.githubusercontent.com/62292136/79073440-9119c780-7d21-11ea-898c-c4e0184777eb.PNG">     
     
     
     
     
## 5. 협동 작업
### 1. push
로컬 저장소에 commit 되어있는 있는 파일들을 원격 저장소로 추가     
사용 방법 : git push -u origin master     
     
     
     
     
     
     
     
     
     
     
# 3. 실습 예제
### 1. github.com 로그인 후 project1 repository 생성
<img width="945" alt="project1생성" src="https://user-images.githubusercontent.com/62292136/79070750-c2d76200-7d12-11ea-9800-48ef186cbc3a.PNG">     
     
### 2. peace서버 로그인
<img width="529" alt="peace서버 로그인" src="https://user-images.githubusercontent.com/62292136/79070788-dd114000-7d12-11ea-82d3-eba90cc4c74d.PNG">     
     
### 3. git global 값 초기화
<img width="559" alt="가git_global_초기화" src="https://user-images.githubusercontent.com/62292136/79070800-f3b79700-7d12-11ea-87ce-b66e923d365a.PNG">     
     
### 4. project directory에서 git repository 생성
<img width="573" alt="git_init" src="https://user-images.githubusercontent.com/62292136/79070819-03cf7680-7d13-11ea-96f6-9a868dd4b9ef.PNG">     
     
### 5. 소스파일 staging area에 등록
<img width="573" alt="git_add" src="https://user-images.githubusercontent.com/62292136/79070832-19dd3700-7d13-11ea-85d3-6386bcc1c48d.PNG">     
     
### 6. staging area의 소스파일 local repository로 commit
<img width="501" alt="커밋" src="https://user-images.githubusercontent.com/62292136/79070883-645eb380-7d13-11ea-8a1a-296948aa00b8.PNG">
     
### 7. remote repository 등록
<img width="502" alt="git_remote_add" src="https://user-images.githubusercontent.com/62292136/79070900-7fc9be80-7d13-11ea-9cc9-f5cac487bd45.PNG">     
     
### 8. remote repository로 push
<img width="482" alt="git_push_origin_master" src="https://user-images.githubusercontent.com/62292136/79070917-9243f800-7d13-11ea-921b-67d5e11f4f66.PNG">
<img width="904" alt="git파일업로드완료" src="https://user-images.githubusercontent.com/62292136/79070928-a25bd780-7d13-11ea-88f4-51992403a30f.PNG">
     
### 9. 소스파일의 Update기능 추가 후 다시 6번, 8번 실행
<img width="947" alt="수정후_commit" src="https://user-images.githubusercontent.com/62292136/79071267-df28ce00-7d15-11ea-8f4a-a0f09210a87f.PNG">     

* 저장된 remote repository(Github)에서 commit 버튼 클릭 후 commit 종류 선택하면 이전 commit과의 차이점을 볼 수 있음     
<img width="943" alt="깃허브_diff_update" src="https://user-images.githubusercontent.com/62292136/79073803-852f0500-7d23-11ea-851b-fa26a92ad401.PNG">     
     
<img width="849" alt="깃허브_diff_update2" src="https://user-images.githubusercontent.com/62292136/79073805-86f8c880-7d23-11ea-826f-2494c26d9f7a.PNG">     
     
     

     
### 10. 소스파일의 Delete기능 추가 후 다시 6번, 8번 실행
<img width="948" alt="delete기능추가후commit" src="https://user-images.githubusercontent.com/62292136/79071257-c6b8b380-7d15-11ea-9155-0de98fced493.PNG">     
     
* 저장된 remote repository(Github)에서 commit 버튼 클릭 후 commit 종류 선택하면 이전 commit과의 차이점을 볼 수 있음     
<img width="943" alt="깃허브_diff_delete" src="https://user-images.githubusercontent.com/62292136/79073769-5022b280-7d23-11ea-918c-e20b2e519a0c.PNG">     
     
<img width="859" alt="깃허브_diff_delete2" src="https://user-images.githubusercontent.com/62292136/79073771-5153df80-7d23-11ea-887c-0589a742f27a.PNG">     
     
     
     

     
### 11. 소스파일의 파일명을 변경 후 다시 6번, 8번 실행
<img width="947" alt="mv_결과" src="https://user-images.githubusercontent.com/62292136/79071287-ed76ea00-7d15-11ea-897f-f953c9e86071.PNG">     

* 저장된 remote repository(Github)에서 commit 버튼 클릭 후 commit 종류 선택하면 이전 commit과의 차이점을 볼 수 있음     
<img width="939" alt="깃허브_diff_renamed" src="https://user-images.githubusercontent.com/62292136/79073728-12be2500-7d23-11ea-9dee-f02e74a601b4.PNG">     
     
     
     
     
     

    
