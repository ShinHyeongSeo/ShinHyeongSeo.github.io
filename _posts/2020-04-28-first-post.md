---
title: "Linux Utility 정리"
date: 2020-04-28 20:36:28 -0000
categories: Linux Utility OSS
---
     
     

# 1. Network 관련 utility
## 1. ifconfig
리눅스 네트워크 인터페이스 설정 및 확인하는 명령어     
       
### ifconfig
현재 활성화된 모든 네트워크 인터페이스의 정보 출력한다. (활성화되어있지 않은 네트워크 인터페이스의 정보는 출력 X)          
<img width="713" alt="ifconfig" src="https://user-images.githubusercontent.com/62292136/80867017-dbf98000-8ccc-11ea-86ac-b11bc1736ce5.PNG">     
     
     
     
### ifconfig -a
활성화되어있지 않은 네트워크 인터페이스를 포함한 모든 네트워크 인터페이스의 정보 출력한다.     
<사진>     
     
### ifconfig [인터페이스명]
입력한 네트워크 인터페이스의 정보만 출력한다.          
<사진>     
     
### ifconfig [인터페이스명] [Up/Down]
입력한 네트워크 인터페이스를 활성화/비활성화한다.     
<사진>     
     
### ifconfig [인터페이스명] [IP 주소]
입력한 네트워크 인터페이스의 IP주소를 설정한다.          
<사진>     
     
### ifconifg [인터페이스명] netmask [subnetmask 값]
입력한 네트워크 인터페이스의 subnetmask 값을 설정한다.     
<사진>     
     
### ifconifg [인터페이스명] broadcast [broadcast 주소]
입력한 네트워크 인터페이스의 broadcast 주소를 설정한다.     
<사진>     
     
### ifconifg [인터페이스명] [IP 주소] netmask [subnetmask 값] broadcast [broadcast 주소]     
입력한 네트워크 인터페이스의 IP주소와 subnetmask 값 broadcast 주소를 한꺼번에 설정한다.     
<사진>     
     
     
## 2. ip
ip주소를 설정하거나 ip주소의 정보를 조회한다.     
     
### ip addr show
ip주소를 출력한다.     
     
### ip route show
라우팅 정보를 출력한다.     
     
## 3. netstat
네트워크 연결상태, 라우팅 테이블, 인터페이스 상태를 출력한다.     
     
### netstat -a
모든 네트워크의 상태를 출력한다.     
     
### netstat -c
모든 네트워크의 상태를 매초마다 갱신하여 출력한다.     
     
### netstat -i
모든 네트워크의 상태를 인터페이스 별로 출력한다.     
     
### netstat -r
라우팅 테이블 정보를 출력한다.     
    
### netstat -s
네트워크 프로토콜 별 통계를 출력한다.     
     
### netstat -V
버전을 출력한다.     
     

## 4. host
host명을 통해서 정보를 조회할 때 사용하는 명령어     
     
### host [host명]
간단하게 IP주소와 메일을 보여준다.     
<사진>     
     
### host [-a] [host명]
도메인 정보를 타입별로 자세하게 보여준다.     
<사진>     
     
### host [-t] [타입] [host명]
도메인 정보를 입력한 타입에 따라서 해당하는 정보만 보여준다.     
<사진>     
     
### host [-v] [host명]
도메인 정보를 자세하게 출력한다.     
<사진>     
     
## 5. hostname
시스템에 설정된 호스트명을 확인하거나 호스트명을 변경할 때 사용한다.     
     
### hostname
호스트명을 출력한다.     
<사진>     
     
### hostname -a
호스트명의 별칭을 출력한다.     
<사진>     
     
### hostname -d
호스트명의 도메인명을 출력한다.     
<사진>     
     
### hostname -f
호스트명의 풀네임을 출력한다.     
<사진>     
     
### hostname -i
호스트명에 설정된 ip주소를 출력한다.     
<사진>     
     
### hostname -V
호스트명의 버전을 출력한다.     
<사진>     
     
## 6. ethtool
## 7. traceroute
입력한 Ip주소나 도메인 까지의 네트워크 경로를 출력한다.     
### traceroute [Ip주소] or [도메인명]
<사진>     
     
### traceroute -m [홉의 수] [Ip주소] or [도메인명]
최대 홉의 수를 지정해서 지정한 수의 홉만큼만 네트워크 경로를 출력한다.     
<사진>     
     
### traceroute -V
traceroute의 버전을 출력한다.     
<사진>     
     
    
# 2. Domain name 관련 utility
     
## 1. nslookup
입력한 Ip주소나 도메인의 정보를 출력한다.     
     
### nslookup [Ip주소]
입력한 Ip주소에 해당하는 도메인의 정보를 출력한다.
<사진>     
     
### nslookup [도메인명]
입력한 도메인의 Ip주소를 출력한다.     
<사진>     
     
### nslookup -type=a [도메인명]
입력한 도메인의 Ip주소를 Ipv4형식으로 출력한다. (기본값)     
     
### nslookup -type=aaaa [도메인명]
입력한 도메인의 Ip주소를 Ipv6형식으로 출력한다.     
     
### nslookup -type=MX [도메인명]
입력한 도메인의 메일서버의 정보를 출력한다.     
     
### nslookup -type=NS [도메인명]
입력한 도메인의 네임서버의 정보를 출력한다.     
     
### nslookup -type=SOA [도메인명]
입력한 도메인의 마스터네임서버의 정보를 출력한다.  
     
     
## 2. ping
상대 호스트와의 연결 가능 여부를 출력한다.     
     
### ping [ip주소] or [도메인명]
입력한 ip주소나 도메인으로 ping을 보낸다.     
     
### ping -c [횟수] [ip주소] or [도메인명]
입력한 ip주소나 도메인으로 ping을 입력한 횟수만큼 보낸다.     
     
### ping -i [초] [ip주소] or [도메인명]
입력한 ip주소나 도메인으로 ping을 입력한 초마다 새로 보낸다.     
     
     













