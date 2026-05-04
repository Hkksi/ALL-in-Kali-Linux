# ALL-in-Kali-Linux

## #개요

2025년 09월 15일부터 11월 28일까지 진행한 CAUtion 프로젝트로, Kali Linux 2025.02에서 새롭게 도입된 MITRE ATT&CK 프레임워크 분류 기준에 따라 취약한 머신을 대상으로 모의해킹을 수행하고 보고서를 작성하는 프로젝트

## #프로젝트원

|기수|이름|
|---|---|
|0기|김하람|
|1기|홍석현|
|7기|고형인|
|7기|정지윤|

## #프로젝트 일정

| 주차 | 프로젝트 기간 | 내용 |
| --- | --- | --- |
| 3주차 | 2025년 9월 15일 ~ 2025년 9월 21일  | OT 및 환경 구축 |
| 4주차 | 2025년 9월 22일 ~ 2025년 9월 28일   | MITRE ATT&CK 프레임워크Machine 공부 및 구축 |
| 5주차 | 2025년 9월 29일 ~ 2025년 10월 5일  | 01 - Reconnaissance |
| 6주차 | 2025년 10월 6일 ~ 2025년 10월 12일  | 02 - Resource Development |
| 7주차 | 2025년 10월 13일 ~ 2025년 10월 19일  | 중간고사 기간 |
| 8주차 | 2025년 10월 20일 ~ 2025년 10월 26일  | 중간고사 기간 |
| 9주차 | 2025년 10월 27일 ~ 2025년 11월 2일  | 03 - Initial Access / 04 - Execution |
| 10주차 | 2025년 11월 3일 ~ 2025년 11월 9일  | 05 - Persistence / 06 - Privilege Escalation |
| 11주차 | 2025년 11월 10일 ~ 2025년 11월 16일  | 07 - Defense Evasion / 08 - Credential Access |
| 12주차 | 2025년 11월 17일 ~ 2025년 11월 23일  | 09 - Discovery / 10 - Lateral Movement |
| 13주차 | 2025년 11월 24일 ~ 2025년 11월 30일  | 11 - Collection / 12 - Command and Control |
| 14주차 | 2025년 12월 1일 ~ 2025년 12월 7일  | 13 - Exfiltration / 14 - Impact |
| 15주차 | 2025년 12월 8일 ~ 2025년 12월 14일  | 기말고사 기간 |
| 16주차 | 2025년 12월 15일 ~ 2025년 12월 21일  | 기말고사 기간 |


## #프로젝트 과정

1. MITRE ATT&CK 프레임워크 이해
    - https://attack.mitre.org/matrices/enterprise
    - https://www.igloo.co.kr/security-information/mitre-attck-framework-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0/
    
2. 모의해킹 환경 구축
    - 모의해킹 대상
        - SPACE-PENTEST
        - Metasploitable 2
3. Kali Linux 2025.2 분류별 도구 조사 및 가상 환경에 적용하여 모의해킹 후 보고서 작성
    -  MITRE ATT&CK Matrix에 제공하는 분류에 맞추어 모의해킹 진행


## #Tools in Kali Linux (2025.2) by MITRE ATT&CK

|  | 01 - Reconnaissance | 02 - Resource Development | 03 - Initial Acess | 04 - Execution | 05 - Persistence | 06 - Privilege Escalation | 07 - Defense Evasion | 08 - Credential Access | 09 - Discovery | 10 - Lateral Movement | 11 - Collection | 12 - Command and Control | 13 - Exfiltration | 14 - Impact |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Bluetooth/spooftooph | clang | commix | metasploit-framework | laudanum | linpeas | Pass-the-Hash/evil-winrm | Brute Force/hydra | Account Discovery/smtp-user-enum | Pass-the-Hash/evil-winrm | ettercap-pkexec | Application Layer Protocol/cadaver | impacket-smbserver | scapy |
| 2 | Host Information/spiderfoot | clang++ | dns-rebind | powersploit | webshells | metasploit-framework | Pass-the-Hash/impacket-scripts | Brute Force/medusa | Active Directory/bloodhound-python | Pass-the-Hash/impacket-scripts | mitmproxy | Application Layer Protocol/evil-winrm | netcat |  |
| 3 | Network Information/amass | generic_chunked | gophish |  | weevely | peass | Pass-the-Hash/mimikatz | Brute Force/ncrack | Databases/impacket-mssqlclient | Pass-the-Hash/mimikatz | ssldump | Application Layer Protocol/impacket-scripts |  |  |
| 4 | Network Information/dmirty | generic_listen_tcp | metasploit-framework |  |  | unix-privesc-check | Pass-the-Hash/netexec | Brute Force/netexec | Databases/mysql | Pass-the-Hash/netexec | sslsplit | Application Layer Protocol/minicom |  |  |
| 5 | Network Information/legion | generic_send_tcp | setoolkit |  |  | winpeas | Pass-the-Hash/passing-the-hash | Brute Force/patator | Databases/sqlitebrowser | Pass-the-Hash/passing-the-hask |  | Application Layer Protocol/netexec |  |  |
| 6 | Network Information/nmap | generic_send_udp | sqlmap |  |  |  | Pass-the-Hash/smbmap | Brute Force/the-pptp-bruter | Network Security Appliances/tcpreplay | Pass-the-Hash/smbmap |  | Application Layer Protocol/smbclient |  |  |
| 7 | Network Information/theHarvester | msf-nasm_shell |  |  |  |  | Pass-the-Hash/xfreerdp3 | Hash Identification/hashid | Network Security Appliances/wafw00f | Pass-the-Hash/xfreedp3 |  | Application Layer Protocol/xfreerdp3 |  |  |
| 8 | Network Information/unicornscan | msfpc |  |  |  |  | exe2hex | Hash Identification/hash-identifier | Network Service Discovery/amass | evil-winrm |  | Non-Application Layer Protocol/dbd |  |  |
| 9 | Network Information/zenmap | msfvenom |  |  |  |  | macchanger | OS Credential Dumping/chntpw | Network Service Discovery/ike-scan | impacket-psexec |  | Non-Application Layer Protocol/netcat |  |  |
| 10 | Network Information:DNS/dnsenum | radare2 |  |  |  |  | msfvenom | OS Credential Dumping/creddump7 | Network Service Discovery/masscan | impacket-smbexec |  | Non-Application Layer Protocol/sbd |  |  |
| 11 | Network Information:DNS/dnsmap | searchsploit |  |  |  |  |  | OS Credential Dumping/mimikatz | Network Service Discovery/nmap |  |  | Non-Application Layer Protocol/socat |  |  |
| 12 | Network Information:DNS/dnsrecon |  |  |  |  |  |  | OS Credential Dumping/samdump2 | Network Service Discovery/unicornscan |  |  | Protocol Tunneling/dns2tcpc |  |  |
| 13 | Vulnerability Scanning/nmap |  |  |  |  |  |  | Password Cracking/hashcat | Network Service Discovery/zenmap |  |  | Protocol Tunneling/dns2tcpd |  |  |
| 14 | Vulnerability Scanning/zenmap |  |  |  |  |  |  | Password Cracking/john | Network Share Discovery/enum4linux |  |  | Protocol Tunneling/iodine-client-start |  |  |
| 15 | Web Scanning/dirb |  |  |  |  |  |  | Password Cracking/ophcrack | Network Share Discovery/nbtscan |  |  | Protocol Tunneling/mifdco |  |  |
| 16 | Web Scanning/dirbuster |  |  |  |  |  |  | Password Profiling & Wordlists/cewl | Network Share Discovery/netexec |  |  | Protocol Tunneling/proxychains4 |  |  |
| 17 | Web Scanning/ffuf |  |  |  |  |  |  | Password Profiling & Wordlists/crunch | Network Share Discovery/smbclient |  |  | Protocol Tunneling/proxytunnel |  |  |
| 18 | Web Scanning/gobuster |  |  |  |  |  |  | Password Profiling & Wordlists/rsmangler | Network Share Discovery/smbmap |  |  | Protocol Tunneling/ptunnel |  |  |
| 19 | Web Scanning/lbd |  |  |  |  |  |  | Password Profiling & Wordlists/wordlists | Network Sniffing/arpspoof |  |  | Protocol Tunneling/pwnat |  |  |
| 20 | Web Scanning/recon-ng |  |  |  |  |  |  | WiFi/aircrack-ng | Network Sniffing/dnschef |  |  | Protocol Tunneling/sslh |  |  |
| 21 | Web Scanning/wfuzz |  |  |  |  |  |  | WiFi/bully | Network Sniffing/dsniff |  |  | Protocol Tunneling/stunnel4 |  |  |
| 22 | Web Vulnerability Scanning/burpsuite |  |  |  |  |  |  | WiFi/fern-wifi-cracker | Network Sniffing/netsniff-ng |  |  | Protocol Tunneling/udptunnel |  |  |
| 23 | Web Vulnerability Scanning/davtest |  |  |  |  |  |  | WiFi/pixiewps | Network Sniffing/scapy |  |  | metasploit-framwork |  |  |
| 24 | Web Vulnerability Scanning/nikto |  |  |  |  |  |  | WiFi/reaver | Network Sniffing/tcpdump |  |  | powershell-empire |  |  |
| 25 | Web Vulnerability Scanning/skipfish |  |  |  |  |  |  | WiFi/wifite | Network Sniffing/wireshark |  |  | starkiller |  |  |
| 26 | Web Vulnerability Scanning/wapiti |  |  |  |  |  |  | cewl | Remote System Discovery/ |  |  |  |  |  |
| 27 | Web Vulnerability Scanning/whatweb |  |  |  |  |  |  | responder | Remote System Discovery/airping |  |  |  |  |  |
| 28 | Web Vulnerability Scanning/wpscan |  |  |  |  |  |  |  | Remote System Discovery/atk6-thcping6 |  |  |  |  |  |
| 29 | WiFi/kismet |  |  |  |  |  |  |  | Remote System Discovery/fierce |  |  |  |  |  |
| 30 | WiFi/wash |  |  |  |  |  |  |  | Remote System Discovery/fping |  |  |  |  |  |
| 31 | maltego |  |  |  |  |  |  |  | Remote System Discovery/hping3 |  |  |  |  |  |
| 32 |  |  |  |  |  |  |  |  | SMTP/smtp-user-enum |  |  |  |  |  |
| 33 |  |  |  |  |  |  |  |  | SMTP/swaks |  |  |  |  |  |
| 34 |  |  |  |  |  |  |  |  | SNMP/onesistyone |  |  |  |  |  |
| 35 |  |  |  |  |  |  |  |  | SNMP/snmp-check |  |  |  |  |  |
| 36 |  |  |  |  |  |  |  |  | SSL/TLS/sslscan |  |  |  |  |  |
| 37 |  |  |  |  |  |  |  |  | SSL/TLS/sslyze |  |  |  |  |  |
| 38 |  |  |  |  |  |  |  |  | System Network Configuration Discovery/netdiscover |  |  |  |  |  |
| 39 |  |  |  |  |  |  |  |  | System Network Configuration Discovery/netmask |  |  |  |  |  |
| 40 |  |  |  |  |  |  |  |  | VoIP/voiphopper |  |  |  |  |  |
