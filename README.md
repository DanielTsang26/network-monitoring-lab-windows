<h1 = align=center>NETWORK MONITORING LAB </h1>

<p align="center">
<img width="756" height="883" alt="Untitled Diagram drawio (3)" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/windows_network_lab.png" />
</p>

## 📌 Introduction

This lab introduces essential network administration tasks such as system logging and traffic monitoring.

## 🛠️ TECHNOLOGY & TOOLS UTILIZED
- **`VirtualBox:`**  
  Used as the primary virtualization platform to host multiple virtual machines in an isolated local environment for cybersecurity testing and infrastructure simulation.

- **`Event Viewer:`**
  Allows the user to view various log types, include application, security, and system logs. These logs can be archived for later review and can be used to spot network trends and provide data for creating
  baselines.

- **`OS/Platform:`**  
  Windows 10 ISO

- **`Wireshark Pro:`**  
  An advanced network protocol analyzer used for deep packet inspection, traffic analysis, and troubleshooting in real-time.

  ## OBJECTIVES:

The objective of the Network Monitoring Lab is to provide hands-on experience in configuring and monitoring essential network services. 
Specifically this lab aims to:

- Understand different types of log files and their purpose
- Examine the application, security, and system logs
- Access the log files stored on a computer system
- TCP/ UDP segmentation to understand where the packets are coming from and where they are going to.

## Step-by-step- Instruction:

### Step 1: Open Event Viewer
After logging into the virtual machine with the platform in Windows 10 OS, open the event viewer. The  Event Viewer application allows you to view various log types, includign application, security, and system logs. These logs can be archived for alter review and can be used to spot network trends and provide data for creating baseline.

<img width="531" height="521" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab.png" /></br>

### Step 2: View Event Viewer

Navigate to the Windows Logs and examine Application, Security, and System logs. Application, security, and system logs provide a detailed record of events and activities occuring on a Windows systems. It helps users to diagnose problems, track applications or system issues, and identify security-related events.  By reviewing these logs, users can gain inisghts into the operation and health of their system, as well as address any potential issues or security concerns that may arise.

**Application:**

<img width="631" height="621" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab3.png" /></br>


**Security:**

<img width="631" height="621" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab4.png" /></br>

**System:**

<img width="631" height="621" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab5.png" /></br>

## Step 4: Saving Logs

Right-click System and select the Save All Events As option. Type the file name and save it in the Documents folder. At the Display Information prompt, click Ok. After that, close all the windows.

<img width="631" height="621" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab6.png" /></br>

## Step 5: Capturing the Structure of a TCP/UDP Segment

Diagram of a TCP Segment:

<img width="431" height="421" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab7.png" /></br>


Diagram of a UDP Segment:

<img width="431" height="421" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab12.png" /></br>

Launch Wireshark and capture packets for the Ethernet0 interface by hitting the Start capturing packets.

<img width="931" height="921" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab8.png" /></br>

After a short period of time between 1 to 2 minutes, Wireshark captures the packets. When you observe the TCP packets, click the Stop capturing packets icon.



## Step 6: Viewing the Structure of the TCP Segment

In the Packet list pane, select any TCP protocol packet.

<img width="931" height="921" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab9.png" /></br>

Double click the TCP to expand the packet to be able to display more information.


<img width="731" height="721" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab10.png" /></br>


<img width="631" height="621" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab11.png" /></br>

## Step 7: Capturing the Structure of a TCP/UDP Segment (For UDP Segment)

Launch Wireshark and capture packets for the Ethernet0 interface by hitting the Start capturing packets.

<img width="931" height="921" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab8.png" /></br>

After a short period of time between 1 to 2 minutes, Wireshark captures the packets. When you observe the TCP packets, click the Stop capturing packets icon.

## Step 8: Viewing the Structure of the UDP Segment

Use the Apply a display filter text box and search `ssdp` to analyze `Hypertext Transfer Protocol (HTTP)` packet.

HTTP packets refer to the packets that are associated with the HTTP protocol. This protocol is used for communication between web browsers and web servers, enabling the transfer of hypertext documents, such as HTML pages.

<img width="931" height="921" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab13.png" /></br>

In the Packet list pane, select any SSDP protocol packet.

<img width="931" height="921" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab14.png" /></br>

Now under the packet details pane, double click User Datagram Protocol to expand the packet and to observe the fields. This information gives a lot of away and it is very important to note that this allows the user to monitor traffic on where this packet comes from in terms of `source port` and  where its going to being the `destination port`. The same goes for the TCP packet as well.

<img width="931" height="921" alt="Lab 1" src="https://raw.githubusercontent.com/DanielTsang26/network-monitoring-lab-windows/refs/heads/main/network_lab15.png" /></br>



---

*This hands-on exercise provided a practical understanding of network health through monitoring and tracking traffic, while also analyzing packets via Wireshark Pro*

### 🔑 Key Takeaways

- Gained hands-on experience with Windows Event Viewer to analyze Application, Security, and System logs for troubleshooting, performance monitoring, and detecting anomalies.
- Learned how to save and archive event logs, enabling long-term analysis and baseline creation for network and system health.
- Captured and analyzed TCP and UDP packets using Wireshark Pro, providing visibility into network communication patterns and protocol behavior.
- Interpreted the structure of TCP/UDP segments, identifying key header fields such as source/destination ports, sequence numbers, and length values.
- Practiced using filters in Wireshark (e.g., ssdp) to isolate specific traffic types, such as HTTP or SSDP, for targeted inspection.
- Developed foundational skills in network traffic inspection and log analysis, critical for security auditing, threat detection, and performance diagnostics.


