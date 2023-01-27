
# Pentesting Project

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

*** '''sudo nmap -sV -p 8787 192.168.1.103*** <br>
result:<br>
The outcome depicts that port 8787 of host 192.168.1.103 is running the service DRB located in folder /usr/lib/ruby/1.8/drb with the version Ruby DRb RMI (Ruby 1.8).

### 2.2 OpenVas
The objective of this task is to scan the requested target, Metasploitable2 VM and generate a vulnerability report. So, I used OpenVAS to scan all TCP ports of the target machine and produced a vulnerability report.
The following steps are implemented to accomplish this task:

Create a port list, target and task.
Under the Configuration tab, click Ports Lists.
Click the Star Icon (on the top left of the screen) to create a New Ports List
Fill out the form with the correct details and click Create.
The created port list should appear on the list, as shown below.
Under the Configuration tab, click Targets.
Click the Star Icon (on the top left of the screen) to create
