---
title: "Git pull을 통한 협업"
date: 2020-05-10 23:45:28 -0000
categories: Git Cowork pull OSS
---





# git pull을 사용해야할 때 #
<br/>
<br/>
<br/>
프로젝트를 함께 진행하고 있는 팀원의 소스가 변경되었을 때     
팀원의 소스를 우리의 Local Repository로 가져와 합쳐야한다.     
이때 쓰는 명령어로 git pull이 있다.     
또, Local Repository로 가져온 다음 다시     
우리의 Remote Git Repository로 push를 해야한다.     
이를 실습을 통해서 진행해보도록 하겠다.     
<br/>
<br/>
<br/>   
<br/>   
<br/>   
<br/>   
# 실습 시나리오 #
<br/>
<br/>
<br/>   
1. 기존의 팀원과 함께 참여하고 있는 프로젝트가 저장 되어있는 디렉토리로 이동한다.     
   (이전에 fork와 clone을 마친상태)    
<br/>
<br/>
<br/>
2. 기존에 연결되어있던 나의 Remote Repository와의 연결을 제거한다.
<br/>
<br/>
     * 예) git remote remove origin
<br/>
<br/>
<br/>
3. 팀원의 프로젝트 Remote Repository를 연결한다.
<br/>
<br/>
     * 예) git remote add [팀원의 Remote Repository 주소]
<br/>
<br/>
<br/>
4. 변경된 사항을 pull을 통해 합친다.
<br/>
<br/>
     * 예) git pull origin master
<br/>
<br/>
<br/>
3. 다시 Remote Repository와의 연결을 제거한다. (나의 Remote Repository에 push 되어야하기 때문)
<br/>
<br/>
     * 예) git remote remove origin
<br/>
<br/>
<br/>
4. 새롭게 나의 Remote Repository를 연결한다.     
     * 예) git remote add origin [나의 Remote Repository주소]
<br/>
<br/>
<br/>
5. 나의 Remote Repository로 push 한다.
<br/>
<br/>
     * 예) git push -u origin master
<br/>
<br/>
<br/>
6. Remote Repository에 잘 push 되었는지 확인한 후, Pull Request를 보낸다.
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
     
     
     
     
     
     
     
     
