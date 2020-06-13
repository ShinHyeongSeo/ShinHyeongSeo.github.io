---
title: "Linux Utility 정리"
date: 2020-04-28 20:36:28 -0000
categories: Linux Utility OSS
---
     
     

# 1. Network 관련 utility
<br/>
<br/>
<br/>
## 1. ifconfig
리눅스 네트워크 인터페이스 설정 및 확인하는 명령어     
<br/>
<br/>
### 1) ifconfig
현재 활성화된 모든 네트워크 인터페이스의 정보 출력한다. (활성화되어있지 않은 네트워크 인터페이스의 정보는 출력 X)          
<img width="713" alt="ifconfig" src="https://user-images.githubusercontent.com/62292136/80867017-dbf98000-8ccc-11ea-86ac-b11bc1736ce5.PNG">     
 <br/>
 <br/>
 <br/>
 <br/>
### 3) ifconfig [인터페이스명]
입력한 네트워크 인터페이스의 정보만 출력한다.         
<img width="662" alt="ifconfig_인터페이스" src="https://user-images.githubusercontent.com/62292136/81296269-9bbf4680-90ac-11ea-9f80-23e6d4549acf.PNG">     
 <br/>
 <br/>
 <br/>
 <br/>
### 4) ifconfig [인터페이스명] [Up/Down]
입력한 네트워크 인터페이스를 활성화/비활성화한다.     
 <br/>
 <br/>
 <br/>
 <br/>
### 5) ifconfig [인터페이스명] [IP 주소]
입력한 네트워크 인터페이스의 IP주소를 설정한다.          
<br/>
<br/>
<br/>
<br/>
### 6) ifconifg [인터페이스명] netmask [subnetmask 값]
입력한 네트워크 인터페이스의 subnetmask 값을 설정한다.     
<br/>
<br/>
<br/>
<br/>
### 7) ifconifg [인터페이스명] broadcast [broadcast 주소]
입력한 네트워크 인터페이스의 broadcast 주소를 설정한다.     
<br/>
<br/>
<br/>
<br/>
### 8) ifconifg [인터페이스명] [IP 주소] netmask [subnetmask 값] broadcast [broadcast 주소]     
입력한 네트워크 인터페이스의 IP주소와 subnetmask 값 broadcast 주소를 한꺼번에 설정한다.     
<br/>
<br/>
<br/>
<br/>
<br/>    
## 2. ip
ip주소를 설정하거나 ip주소의 정보를 조회한다.
<br/>
<br/>
<br/>
### 1) ip addr show
ip주소를 출력한다.     
<img width="779" alt="ip_addr_show" src="https://user-images.githubusercontent.com/62292136/80867029-f16eaa00-8ccc-11ea-8764-f7084ef5612d.PNG">
<br/>
<br/>
<br/>
<br/>
### 2) ip route show
라우팅 정보를 출력한다.    
<img width="679" alt="ip_route_show" src="https://user-images.githubusercontent.com/62292136/80867185-b456e780-8ccd-11ea-8190-8bbcc8504647.PNG">  
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
## 3. netstat
네트워크 연결상태, 라우팅 테이블, 인터페이스 상태를 출력한다.
<br/>
<br/>
<img width="949" alt="netstat_1" src="https://user-images.githubusercontent.com/62292136/80867059-13682c80-8ccd-11ea-835c-051aa8932800.PNG">     
<img width="946" alt="netstat_2" src="https://user-images.githubusercontent.com/62292136/80867061-14995980-8ccd-11ea-909a-b6b6af017249.PNG">     
<img width="947" alt="netstat_3" src="https://user-images.githubusercontent.com/62292136/80867062-1531f000-8ccd-11ea-911c-070b9061c1c9.PNG">
<br/>
<br/>
<br/>
<br/>
<br/>     
### 1) netstat -c
모든 네트워크의 상태를 매초마다 갱신하여 출력한다.    
netstat을 입력했을 때의 화면이 매초마다 갱신된다.
<br/>
<br/>
<br/>
### 2) netstat -i
모든 네트워크의 상태를 인터페이스 별로 출력한다.     
<img width="811" alt="netstat_i" src="https://user-images.githubusercontent.com/62292136/80867080-2d097400-8ccd-11ea-9503-015e00db10ef.PNG">
<br/>
<br/>
<br/>
<br/>
### 3) netstat -r
라우팅 테이블 정보를 출력한다.     
<img width="781" alt="netstat_r" src="https://user-images.githubusercontent.com/62292136/80867091-372b7280-8ccd-11ea-846e-379ec9e1a7b5.PNG">
<br/>
<br/>
<br/>
<br/>   
### 4) netstat -s
네트워크 프로토콜 별 통계를 출력한다.     
<img width="948" alt="netstat_s_1" src="https://user-images.githubusercontent.com/62292136/80867096-414d7100-8ccd-11ea-837c-a95251cb8eea.PNG">     
<img width="945" alt="netstat_s_2" src="https://user-images.githubusercontent.com/62292136/80867097-41e60780-8ccd-11ea-8cf2-7bc54cb8bbd0.PNG">     
<img width="950" alt="netstat_s_3" src="https://user-images.githubusercontent.com/62292136/80867099-427e9e00-8ccd-11ea-8d20-8eff39dd8718.PNG">
<br/>
<br/>
<br/>
<br/>     
### 6) netstat -V
netstat의 버전을 출력한다.     
<img width="848" alt="netstat_V" src="https://user-images.githubusercontent.com/62292136/80867105-4d393300-8ccd-11ea-8806-510089b03122.PNG">     
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>     
## 4. host
host명을 통해서 정보를 조회할 때 사용하는 명령어     
<br/>
<br/>
<br/>   
### 1) host [host명]
간단하게 IP주소와 메일서버를 보여준다.     
<img width="723" alt="host" src="https://user-images.githubusercontent.com/62292136/80867148-870a3980-8ccd-11ea-88db-470563796969.PNG"> <br/>
<br/>
<br/>
<br/>     
### 2) host [-a] [host명]
도메인 정보를 타입별로 자세하게 보여준다.     
<img width="946" alt="host_a" src="https://user-images.githubusercontent.com/62292136/80867150-883b6680-8ccd-11ea-9eab-8f8b43ab58fc.PNG">     
<br/>
<br/>
<br/>
<br/>     
### 3) host [-t] [타입] [host명]
도메인 정보를 입력한 타입에 따라서 해당하는 정보만 보여준다.   
A : 도메인 IP주소     
<img width="519" alt="host_t_A" src="https://user-images.githubusercontent.com/62292136/81295685-c230b200-90ab-11ea-97f8-f7469cc2da38.PNG">     
<br/>
<br/>
<br/>
<br/>  
NS : 호스트 네임서버 호스트     
<img width="513" alt="host_t_NS" src="https://user-images.githubusercontent.com/62292136/81295687-c361df00-90ab-11ea-9215-60023b872043.PNG">     
<br/>
<br/>
<br/>
<br/>   
PTR : 도메인 네임 포인터     
<img width="462" alt="host_t_PTR" src="https://user-images.githubusercontent.com/62292136/81295688-c361df00-90ab-11ea-8e83-5a37be0bc746.PNG">  
<br/>
<br/>
<br/>
<br/>     
### 4) host [-V] [host명]
호스트의 버전을 출력한다.    
<img width="447" alt="host_V" src="https://user-images.githubusercontent.com/62292136/81296136-6c103e80-90ac-11ea-805d-94a0fcd613a5.PNG">    
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>     
## 5. hostname
시스템에 설정된 호스트명을 확인하거나 호스트명을 변경할 때 사용한다.
<br/>
<br/>
### 1) hostname
호스트명을 출력한다.     
<img width="487" alt="hostname" src="https://user-images.githubusercontent.com/62292136/80867213-e8caa380-8ccd-11ea-8187-644d1ee9cdcf.PNG">
<br/>
<br/>
<br/>
<br/>
### 2) hostname -i
호스트명에 설정된 ip주소를 출력한다.     
<img width="484" alt="hostname_i" src="https://user-images.githubusercontent.com/62292136/80867214-e9fbd080-8ccd-11ea-8745-26953839cf3c.PNG">
<br/>
<br/>
<br/>
<br/>          
### 3) hostname -V
호스트명의 버전을 출력한다.     
<img width="484" alt="hostname_V" src="https://user-images.githubusercontent.com/62292136/80867215-e9fbd080-8ccd-11ea-954d-20ef321e7f0b.PNG">  
<br/>
<br/>
<br/>
<br/>     
### 4) hostname -a
호스트명의 별칭을 출력한다.
<br/>
<br/>
<br/>
<br/>
### 5) hostname -d
호스트명의 도메인명을 출력한다.
<br/>
<br/>
<br/>
<br/>   
### 6) hostname -f
호스트명의 풀네임을 출력한다.
<br/>
<br/>
<br/>
<br/>     
## 6. ethtool
네트워크 인터페이스의 정보를 출력, 설정, 관리하는 명령어이다.
<br/>
<br/>
### 1) ethtool [인터페이스명]
<img width="681" alt="ethtool" src="https://user-images.githubusercontent.com/62292136/81187329-dd89b780-8fee-11ea-844d-6d30ab722070.PNG">     
<br/>
<br/>
<br/>
<br/>     
### 2) ethtool -S [인터페이스명]
인터페이스 통계정보를 출력한다.     
<img width="673" alt="ethtool_S_1" src="https://user-images.githubusercontent.com/62292136/81298785-3d946280-90b0-11ea-9bbb-69edbab3e43c.PNG">
<br/>
<br/>
<br/>
<br/>
<img width="733" alt="ethtool_S_2" src="https://user-images.githubusercontent.com/62292136/81298788-3ec58f80-90b0-11ea-8c77-fb4a09ad5e2e.PNG">
<br/>
<br/>
<br/>
<br/>
### 3) ethtool -i [인터페이스명]
인터페이스 드라이버 정보를 출력한다.     
<img width="681" alt="ethtool" src="https://user-images.githubusercontent.com/62292136/81298653-0aea6a00-90b0-11ea-8869-e38a8ea7afd0.PNG"> 
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>     
## 7. traceroute
입력한 Ip주소나 도메인 까지의 네트워크 경로를 출력한다.
<br/>
<br/>
### 1) traceroute [Ip주소] or [도메인명]   
<img width="748" alt="traceroute" src="https://user-images.githubusercontent.com/62292136/80966797-2b1bee00-8e50-11ea-8470-a31d26943fd8.PNG">      
<br/>
<br/>
<br/>
<br/>
### 2) traceroute -m [홉의 수] [Ip주소] or [도메인명]
최대 홉의 수를 지정해서 지정한 수의 홉만큼만 네트워크 경로를 출력한다.      
<img width="743" alt="traceroute_m" src="https://user-images.githubusercontent.com/62292136/80966798-2c4d1b00-8e50-11ea-9a42-4876cc3c4748.PNG">
<br/>
<br/>
<br/>
<br/>
### 3) traceroute -V
traceroute의 버전을 출력한다.     
<img width="560" alt="traceroute_V" src="https://user-images.githubusercontent.com/62292136/80966800-2ce5b180-8e50-11ea-9949-ce9b49b75571.PNG">  
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>     
# 2. Domain name 관련 utility
<br/>
<br/>
<br/>
<br/>     
## 1. nslookup
입력한 Ip주소나 도메인의 정보를 출력한다.
<br/>
<br/>     
### 1) nslookup [Ip주소]
입력한 Ip주소에 해당하는 도메인의 정보를 출력한다.    
<img width="622" alt="nslookup_IP주소" src="https://user-images.githubusercontent.com/62292136/81295993-33706500-90ac-11ea-9822-a996cb811071.PNG">
<br/>
<br/>
<br/>
<br/>     
### 2) nslookup [도메인명]
입력한 도메인의 Ip주소를 출력한다.
<br/>
<br/>
<img width="481" alt="nslookup" src="https://user-images.githubusercontent.com/62292136/81075816-cb901200-8f25-11ea-9fec-7644c1ed0b0d.PNG">
<br/>
<br/>
<br/>
<br/>
### 3) nslookup -type=a [도메인명]
입력한 도메인의 Ip주소를 Ipv4형식으로 출력한다. (기본값)
<br/>
<br/>
<img width="465" alt="nslookup_type_a" src="https://user-images.githubusercontent.com/62292136/81075820-ccc13f00-8f25-11ea-8169-1631ac720053.PNG"> 
<br/>
<br/>
<br/>
<br/>     
### 4) nslookup -type=aaaa [도메인명]
입력한 도메인의 Ip주소를 Ipv6형식으로 출력한다.
<br/>
<br/>
<img width="627" alt="nslookup_type_aaaa" src="https://user-images.githubusercontent.com/62292136/81075821-ccc13f00-8f25-11ea-91fc-64e055ccc07e.PNG">     
<br/>
<br/>
<br/>
<br/>     
### 5) nslookup -type=MX [도메인명]
입력한 도메인의 메일서버의 정보를 출력한다.
<br/>
<br/>
<img width="739" alt="nslookup_type_MX" src="https://user-images.githubusercontent.com/62292136/81075822-cd59d580-8f25-11ea-9aa3-d2e1da3996a5.PNG">
<br/>
<br/>
<br/>
<br/>
### 6) nslookup -type=NS [도메인명]
입력한 도메인의 네임서버의 정보를 출력한다.
<br/>
<br/>
<img width="655" alt="nslookup_type_NS" src="https://user-images.githubusercontent.com/62292136/81075824-cd59d580-8f25-11ea-9d14-a36c48054932.PNG">
<br/>
<br/>
<br/>
<br/>     
### 7) nslookup -type=SOA [도메인명]
입력한 도메인의 마스터네임서버의 정보를 출력한다.
<br/>
<br/>
<img width="662" alt="nslookup_type_SOA" src="https://user-images.githubusercontent.com/62292136/81075825-cdf26c00-8f25-11ea-8a2b-e0737ccb0471.PNG">
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>     
## 2. ping
상대 호스트와의 연결 가능 여부를 Ctrl+c가 입력될 때까지 출력한다.
<br/>
<br/>
### 1) ping [ip주소] or [도메인명]
입력한 ip주소나 도메인으로 ping을 보낸다.
<br/>
<br/>
<img width="818" alt="ping_1" src="https://user-images.githubusercontent.com/62292136/80867435-e9176e80-8cce-11ea-8502-de240a6d9cee.PNG">
<br/>
<br/>
<br/>
<br/>
### 2) ping -c [횟수] [ip주소] or [도메인명]
입력한 ip주소나 도메인으로 ping을 입력한 횟수만큼 보낸다.
<br/>
<br/>
<img width="725" alt="ping_c" src="https://user-images.githubusercontent.com/62292136/80867436-e9b00500-8cce-11ea-9fee-b1034c932e47.PNG">
<br/>
<br/>
<img width="706" alt="ping_c_2" src="https://user-images.githubusercontent.com/62292136/80867432-e74dab00-8cce-11ea-8545-876363aecc2b.PNG">
<br/>
<br/>
<br/>
<br/>     
### 3) ping -i [초] [ip주소] or [도메인명]
입력한 ip주소나 도메인으로 ping을 입력한 초마다 새로 보낸다.
<br/>
<br/>
<img width="750" alt="ping_i" src="https://user-images.githubusercontent.com/62292136/80867433-e87ed800-8cce-11ea-89c8-48a13a45e4ee.PNG">
<br/>
<br/>     
<img width="645" alt="ping_i_2" src="https://user-images.githubusercontent.com/62292136/80867434-e9176e80-8cce-11ea-918c-a77645f5e3f2.PNG">
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

     
     
     
     













