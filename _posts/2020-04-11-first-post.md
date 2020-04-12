---
title: "Git 명령어 정리"
date: 2020-04-11 17:49:28 -0000
categories: Linux OSS Git
---

# 1. Git 명령어 정리
## 1. 작업 공간 시작       
### 1. init
로컬 저장소로 사용할 폴더를 생성하여 해당 폴더로 이동 후 "git init"을 입력하면 새로운 git저장소가 만들어진다.     
(지금 있는 디렉토리를 git을 통해 버전관리를 하겠다고 지정함)     
     
### 2. clone

     
    
     
     
## 2. 변경 사항에 대한 작업
### 1. add
파일을 staging area에 추가    
git remote add origin <url> reote repository를 등록     
     
### 2. mv
파일 이름 변경
### 3. reset
파일을 현재 버전으로 되돌리기 add무효화 변경된 staging area 무혀화, 가장 최근버전으로 돌아감
### 4. rm     
git과 로컬 디렉토리에서 모두 삭제
     
     
     
## 3. 커밋 내역 표시 및 조작     
### 1. commit
staging area에 파일들을 local repository에 등록
### 2. merge
### 3. branch
### 4. checkout
working directory에서 수정한 파일내용을 다시 수정하기 전으로 되돌리고 싶을 때
### 5. diff
working directory에서 작업한 파일의 내용과 가장 최근에 commit한 파일내용의 차이점을 보여줌
두 개의 값을 입력하면 두 파일간의 차이점을 보여줌
### 6. tag
     
     
     
## 4. 커밋 내역 및 상태보기     
### 1. log
커밋 기록 보기
### 2. status
작업 폴더의 상태를 표시
### 3. show
가장 최근의 커밋 정보 확인     
     
## 5. 협동 작업
### 1. fetch
### 2. pull
### 3. push
local repository에 있는 파일들을 repote repository로 추가     
     
     
     
     
     
# 2. 실습 예제
### 1. github.com 로그인 후 project1 repository 생성
### 2. peace서버 로그인
### 3. git global 값 초기화
### 4. project directory에서 git repository 생성
### 5. 소스파일 staging area에 등록
### 6. staging area의 소스파일 local repository로 commit
### 7. remote repository로 push
### 8. 소스파일의 Update기능 추가 후 다시 5~7번 실행
### 9. 소스파일의 Delete기능 추가 후 다시 5~7번 실행
### 10. 소스파일의 파일명을 변경 후 다시 5~7번 실행



















