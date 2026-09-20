## Reverse-Shell-Bind-Shell-Cybersecurity-Lab

## 📖 Introduction

A shell provides an interface for interacting with an operating system through commands. In cybersecurity, unauthorized shell access can allow an attacker to interact with a compromised system remotely.

This project focuses on understanding two common shell communication concepts: **Reverse Shell** and **Bind Shell**. The practical demonstrations were performed in an isolated lab environment using **Kali Linux** and **Metasploitable 2**.

The project also includes basic network connectivity testing, TCP communication using Netcat, shell verification, and network traffic analysis using Wireshark. The main goal is to understand how these connections work from both an offensive and defensive perspective and how suspicious shell activity can be detected and mitigated.

## 🧪 Lab Environment

This project was performed in an isolated virtual lab environment using the following systems:

| System | Role | IP Address |
|---|---|---|
| Kali Linux | Testing / Listener Machine | 192.168.5.128 |
| Metasploitable 2 | Target / Lab Machine | 192.168.5.129 |

### Network Configuration

Both virtual machines were connected to the same isolated lab network, allowing controlled communication between Kali Linux and Metasploitable 2.

### Environment

- **Operating System:** Kali Linux
- **Target OS:** Metasploitable 2
- **Network:** Isolated Virtual Network
- **Shell Utility:** Netcat (nc)

# 📌 Overview

This project demonstrates the concepts of Reverse Shell and Bind Shell in an isolated cybersecurity lab environment using Kali Linux and Metasploitable 2.
The objective is to understand how shell connections can be established between two systems, how network connections appear during the process, and how defenders can identify suspicious shell activity through network and traffic analysis.
The project also covers basic detection indicators, security risks, and mitigation techniques associated with unauthorized shell connections.


# 🔗 Bind Shell

# Step:-1

Fast check your target system is up & no
open tarminal type (ping -c 4 192.168.5.129)
<img width="722" height="376" alt="image" src="https://github.com/user-attachments/assets/caed70db-30e7-43d2-ad23-75e4d27e35e7" />

# Step:-2

Checking which network ports on traget are ready for incoming connections.
open your target system and Use this command **netstat -tuln**
<img width="712" height="447" alt="image" src="https://github.com/user-attachments/assets/dde233b9-2f1a-4653-b5c6-80ca083f4ab0" />

Like this
Port	Protocol	Simple meaning
21	  TCP	FTP   service commonly
22	  TCP	      SSH
53	TCP/UDP	    DNS
80	TCP	HTTP/Web service

# Step:-4
open kali pc type this command **nc -h** and check Netcat is install.

<img width="975" height="665" alt="image" src="https://github.com/user-attachments/assets/275c13fa-2940-4d2d-a514-05dae9c2223f" />

# Step:-5
type this your kali system **nc -lvnp 4444**

<img width="617" height="110" alt="image" src="https://github.com/user-attachments/assets/f3db4d2a-44d4-4ece-ba53-c276b2d444bf" />

# Step:-6
you Type this command in your target **nc 192.168.5.128 4444**

<img width="555" height="82" alt="image" src="https://github.com/user-attachments/assets/1eaa8792-0dd1-4424-86d4-b9963471d242" />

# Step:-7
Then you type any massage in yor target pc and after check your kali pc receive any massage. 

<img width="560" height="147" alt="image" src="https://github.com/user-attachments/assets/0c7fcd3d-723a-4128-9c2f-9acf3d0bad87" />

<img width="597" height="192" alt="image" src="https://github.com/user-attachments/assets/30ed7c2f-4965-4fbe-b3eb-d0589afc0b33" />

# 🔗 Bind Shell

# Step:-1
this type you kali system (nc -lvnp 4445) 

<img width="491" height="82" alt="image" src="https://github.com/user-attachments/assets/9a194abd-1a20-4e05-ac21-0c43bb216b02" />

# Step:-2
After type this command your target system (nc -lvnp 4445)

<img width="850" height="455" alt="image" src="https://github.com/user-attachments/assets/bf426601-e226-409a-9c67-2e86367185f7" />

Then go your kali pc and type (whoami)

<img width="666" height="287" alt="image" src="https://github.com/user-attachments/assets/038adcdb-2ff0-4c54-9132-53fc50ace3cf" />
<img width="690" height="327" alt="image" src="https://github.com/user-attachments/assets/6a811b43-914c-44fa-87be-22a5bd811bbf" />

## 🏁 Conclusion

This project provided hands-on experience with **Reverse Shell** and **Bind Shell** concepts in a controlled cybersecurity lab environment.
During the lab, I established TCP connections between **Kali Linux and Metasploitable 2** and verified remote shell communication using Netcat.
The project helped me understand the difference between Reverse Shell and Bind Shell, the role of listening ports, TCP communication, and how remote shell connections work.
Overall, this lab strengthened my practical knowledge of **Linux networking, TCP communication, Netcat, and remote shell concepts**.


