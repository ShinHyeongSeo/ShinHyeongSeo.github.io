---
title: "Linux Utility 정리"
date: 2020-04-28 20:36:28 -0000
categories: Linux Utility OSS
---
     
     

# 1. Network 관련 utility
## 1. ifconfig
리눅스 네트워크 인터페이스 설정 및 확인하는 명령어     
       
### 1) ifconfig
현재 활성화된 모든 네트워크 인터페이스의 정보 출력한다. (활성화되어있지 않은 네트워크 인터페이스의 정보는 출력 X)          
<img width="713" alt="ifconfig" src="https://user-images.githubusercontent.com/62292136/80867017-dbf98000-8ccc-11ea-86ac-b11bc1736ce5.PNG">     
     
     
     
### 2) ifconfig -a
활성화되어있지 않은 네트워크 인터페이스를 포함한 모든 네트워크 인터페이스의 정보 출력한다.          
     
### 3) ifconfig [인터페이스명]
입력한 네트워크 인터페이스의 정보만 출력한다.          
     
### 4) ifconfig [인터페이스명] [Up/Down]
입력한 네트워크 인터페이스를 활성화/비활성화한다.     
     
### 5) ifconfig [인터페이스명] [IP 주소]
입력한 네트워크 인터페이스의 IP주소를 설정한다.          
     
### 6) ifconifg [인터페이스명] netmask [subnetmask 값]
입력한 네트워크 인터페이스의 subnetmask 값을 설정한다.     
     
### 7) ifconifg [인터페이스명] broadcast [broadcast 주소]
입력한 네트워크 인터페이스의 broadcast 주소를 설정한다.     
     
### 8) ifconifg [인터페이스명] [IP 주소] netmask [subnetmask 값] broadcast [broadcast 주소]     
입력한 네트워크 인터페이스의 IP주소와 subnetmask 값 broadcast 주소를 한꺼번에 설정한다.     
     
     
## 2. ip
ip주소를 설정하거나 ip주소의 정보를 조회한다.     
     
### 1) ip addr show
ip주소를 출력한다.     
<img width="779" alt="ip_addr_show" src="https://user-images.githubusercontent.com/62292136/80867029-f16eaa00-8ccc-11ea-8764-f7084ef5612d.PNG">     
     
     
### 2) ip route show
라우팅 정보를 출력한다.    
<img width="679" alt="ip_route_show" src="https://user-images.githubusercontent.com/62292136/80867185-b456e780-8ccd-11ea-8190-8bbcc8504647.PNG">     
     
     
     
     
## 3. netstat
네트워크 연결상태, 라우팅 테이블, 인터페이스 상태를 출력한다.     
<img width="949" alt="netstat_1" src="https://user-images.githubusercontent.com/62292136/80867059-13682c80-8ccd-11ea-835c-051aa8932800.PNG">     
<img width="946" alt="netstat_2" src="https://user-images.githubusercontent.com/62292136/80867061-14995980-8ccd-11ea-909a-b6b6af017249.PNG">     
<img width="947" alt="netstat_3" src="https://user-images.githubusercontent.com/62292136/80867062-1531f000-8ccd-11ea-911c-070b9061c1c9.PNG">     
     
     
### 1) netstat -a
모든 네트워크의 상태를 출력한다.     
     
### 2) netstat -c
모든 네트워크의 상태를 매초마다 갱신하여 출력한다.     
     
### 3) netstat -i
모든 네트워크의 상태를 인터페이스 별로 출력한다.     
<img width="811" alt="netstat_i" src="https://user-images.githubusercontent.com/62292136/80867080-2d097400-8ccd-11ea-9503-015e00db10ef.PNG">     
     
     
### 4) netstat -r
라우팅 테이블 정보를 출력한다.     
<img width="781" alt="netstat_r" src="https://user-images.githubusercontent.com/62292136/80867091-372b7280-8ccd-11ea-846e-379ec9e1a7b5.PNG">     
     
    
### 5) netstat -s
네트워크 프로토콜 별 통계를 출력한다.     
<img width="948" alt="netstat_s_1" src="https://user-images.githubusercontent.com/62292136/80867096-414d7100-8ccd-11ea-837c-a95251cb8eea.PNG">     
<img width="945" alt="netstat_s_2" src="https://user-images.githubusercontent.com/62292136/80867097-41e60780-8ccd-11ea-8cf2-7bc54cb8bbd0.PNG">     
<img width="950" alt="netstat_s_3" src="https://user-images.githubusercontent.com/62292136/80867099-427e9e00-8ccd-11ea-8d20-8eff39dd8718.PNG">     
     
     
### 6) netstat -V
버전을 출력한다.     
<img width="848" alt="netstat_V" src="https://user-images.githubusercontent.com/62292136/80867105-4d393300-8ccd-11ea-8806-510089b03122.PNG">     
     
     
     
## 4. host
host명을 통해서 정보를 조회할 때 사용하는 명령어     
     
### 1) host [host명]
간단하게 IP주소와 메일을 보여준다.     
<img width="723" alt="host" src="https://user-images.githubusercontent.com/62292136/80867148-870a3980-8ccd-11ea-88db-470563796969.PNG">       
     
     
### 2) host [-a] [host명]
도메인 정보를 타입별로 자세하게 보여준다.     
<img width="946" alt="host_a" src="https://user-images.githubusercontent.com/62292136/80867150-883b6680-8ccd-11ea-9eab-8f8b43ab58fc.PNG">     
     
     
### 3) host [-t] [타입] [host명]
도메인 정보를 입력한 타입에 따라서 해당하는 정보만 보여준다.     
     
### 4) host [-V] [host명]
호스트의 버전을 출력한다.    
<img width="575" alt="host_V" src="https://user-images.githubusercontent.com/62292136/80867151-88d3fd00-8ccd-11ea-8ff0-4c06d6408842.PNG">     
     
     
## 5. hostname
시스템에 설정된 호스트명을 확인하거나 호스트명을 변경할 때 사용한다.     
     
### 1) hostname
호스트명을 출력한다.     
<img width="487" alt="hostname" src="https://user-images.githubusercontent.com/62292136/80867213-e8caa380-8ccd-11ea-8187-644d1ee9cdcf.PNG">     
     
     
### 2) hostname -a
호스트명의 별칭을 출력한다.      
     
### 3) hostname -d
호스트명의 도메인명을 출력한다.     
     
### 4) hostname -f
호스트명의 풀네임을 출력한다.     
     
### 5) hostname -i
호스트명에 설정된 ip주소를 출력한다.     
<img width="484" alt="hostname_i" src="https://user-images.githubusercontent.com/62292136/80867214-e9fbd080-8ccd-11ea-8745-26953839cf3c.PNG">      
     
     
### 6) hostname -V
호스트명의 버전을 출력한다.     
<img width="484" alt="hostname_V" src="https://user-images.githubusercontent.com/62292136/80867215-e9fbd080-8ccd-11ea-954d-20ef321e7f0b.PNG">     
     
     
## 6. ethtool
## 7. traceroute
입력한 Ip주소나 도메인 까지의 네트워크 경로를 출력한다.     
     
### 1) traceroute [Ip주소] or [도메인명]   
     
### 2) traceroute -m [홉의 수] [Ip주소] or [도메인명]
최대 홉의 수를 지정해서 지정한 수의 홉만큼만 네트워크 경로를 출력한다.         
     
### 3) traceroute -V
traceroute의 버전을 출력한다.     
     
    
# 2. Domain name 관련 utility
     
## 1. nslookup
입력한 Ip주소나 도메인의 정보를 출력한다.     
     
### 1) nslookup [Ip주소]
입력한 Ip주소에 해당하는 도메인의 정보를 출력한다.
     
### 2) nslookup [도메인명]
입력한 도메인의 Ip주소를 출력한다.     
     
### 3) nslookup -type=a [도메인명]
입력한 도메인의 Ip주소를 Ipv4형식으로 출력한다. (기본값)     
     
### 4) nslookup -type=aaaa [도메인명]
입력한 도메인의 Ip주소를 Ipv6형식으로 출력한다.     
     
### 5) nslookup -type=MX [도메인명]
입력한 도메인의 메일서버의 정보를 출력한다.     
     
### 6) nslookup -type=NS [도메인명]
입력한 도메인의 네임서버의 정보를 출력한다.     
     
### 7) nslookup -type=SOA [도메인명]
입력한 도메인의 마스터네임서버의 정보를 출력한다.  
     
     
## 2. ping
상대 호스트와의 연결 가능 여부를 Ctrl+c가 입력될 때까지 출력한다.     
     
### 1) ping [ip주소] or [도메인명]
입력한 ip주소나 도메인으로 ping을 보낸다.     
<img width="818" alt="ping_1" src="https://user-images.githubusercontent.com/62292136/80867435-e9176e80-8cce-11ea-8502-de240a6d9cee.PNG">     
     
     
### 2) ping -c [횟수] [ip주소] or [도메인명]
입력한 ip주소나 도메인으로 ping을 입력한 횟수만큼 보낸다.     
<img width="725" alt="ping_c" src="https://user-images.githubusercontent.com/62292136/80867436-e9b00500-8cce-11ea-9fee-b1034c932e47.PNG">     
     
<img width="706" alt="ping_c_2" src="https://user-images.githubusercontent.com/62292136/80867432-e74dab00-8cce-11ea-8545-876363aecc2b.PNG">     
     
     
### 3) ping -i [초] [ip주소] or [도메인명]
입력한 ip주소나 도메인으로 ping을 입력한 초마다 새로 보낸다.     
<img width="750" alt="ping_i" src="https://user-images.githubusercontent.com/62292136/80867433-e87ed800-8cce-11ea-89c8-48a13a45e4ee.PNG">      
     
<img width="645" alt="ping_i_2" src="https://user-images.githubusercontent.com/62292136/80867434-e9176e80-8cce-11ea-918c-a77645f5e3f2.PNG">     
     
     
     
     













