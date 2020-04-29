---
title: "Linux Utility 정리"
date: 2020-04-28 20:36:28 -0000
categories: Linux Utility OSS
---
     
     

# 1. Network 관련 utility
## 1. ifconfig
리눅스 네트워크 인터페이스 설정 및 확인하는 명령어     
       
### ifconfig : 현재 활성화된 모든 네트워크 인터페이스의 정보 출력 (활성화되어있지 않은 네트워크 인터페이스의 정보는 출력 X)          
<사진>    
     
### ifconfig -a : 활성화되어있지 않은 네트워크 인터페이스를 포함한 모든 네트워크 인터페이스의 정보 출력     
<사진>     
     
### ifconfig [인터페이스명] : 입력한 네트워크 인터페이스의 정보만 출력     
<사진>     
     
### ifconfig [인터페이스명] [Up/Down] : 입력한 네트워크 인터페이스를 활성화/비활성화     
<사진>     
     
### ifconfig [인터페이스명] [IP 주소] : 입력한 네트워크 인터페이스의 IP주소를 설정한다.          
<사진>     
     
### ifconifg [인터페이스명] netmask [subnetmask 값] : 입력한 네트워크 인터페이스의 subnetmask 값을 설정한다.     
<사진>     
     
### ifconifg [인터페이스명] broadcast [broadcast 주소] : 입력한 네트워크 인터페이스의 broadcast 주소를 설정한다.     
<사진>     
     
### ifconifg [인터페이스명] [IP 주소] netmask [subnetmask 값] broadcast [broadcast 주소]     
: 입력한 네트워크 인터페이스의 IP주소와 subnetmask 값 broadcast 주소를 한꺼번에 설정한다.     
<사진>     
     
     
## 2. ip

## 3. netstat
## 4. host
## 5. hostname
## 6. ethtool
## 7. traceroute      
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
# 2. Domain name 관련 utility
## 1. nslookup
## 2. ping
