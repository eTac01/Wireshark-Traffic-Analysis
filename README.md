# Task 5: Network Traffic Analysis

## Objective
To capture live network traffic using Wireshark and identify basic protocols.

## Steps Performed
1. Installed Wireshark.
   
Go to 
```
  https://www.wireshark.org/download.html
```
Download the Windows Installer (64-bit).

Run the installer → click Next on all steps.

When asked to install Npcap, select “Install Npcap” (important for packet capture).

 for Linux

 ``` 
     sudo apt update
     sudo apt install wireshark -y

```
Then, add your user to the Wireshark group:
```
sudo usermod -aG wireshark $USER

```

Restart your system.

Launch Wireshark after installation.

Open Wireshark.

You’ll see a list of network interfaces (like eth0, wlan0, Wi-Fi, etc.).

Identify your active network interface (the one with live packet counts).

Click on it to start capturing.

2. Captured packets from Wi-Fi interface while browsing websites.

   While Wireshark is capturing:

Open a browser and visit a few websites (like example.com or ```openai.com```),
OR

Run a ping command:

```
    ping google.com -c 5
```
  
3. Filtered traffic by HTTP, DNS, and TCP.

   You can filter by protocol using the Display Filter Bar (top of Wireshark window):

Protocol	Filter Command	Description
    HTTP	    http	        Shows web traffic

<img width="797" height="236" alt="image" src="https://github.com/user-attachments/assets/2f3af28e-12ca-4554-ab42-bb2e515ff23d" />

    
   # DNS	      dns          	Shows domain name requests
   
<img width="1643" height="412" alt="image" src="https://github.com/user-attachments/assets/8addfb35-3c05-4c7e-802f-64b00da9cb4f" />

   
  #  TCP	      tcp	          Shows Transmission Control Protocol packets

  <img width="1643" height="412" alt="image" src="https://github.com/user-attachments/assets/a5d59cfb-f2b2-4385-8fe3-82a9a1d52523" />

  #  UDP	      udp	          Shows User Datagram Protocol packets

  <img width="1643" height="412" alt="image" src="https://github.com/user-attachments/assets/530e0589-231a-4347-a29c-1985c9028e28" />

  #  ICMP	    icmp	        Shows ping packets

<img width="1643" height="412" alt="image" src="https://github.com/user-attachments/assets/51919ae6-83a6-476b-b458-ca1c39f51a07" />

Try each filter and note down what you see.


# 5. Saved the capture as .pcap.
 saved file 

 <img width="627" height="468" alt="image" src="https://github.com/user-attachments/assets/e9c9c664-495c-4072-9688-da59dc6f25c4" />

## Protocols Identified
- **HTTP:** Web traffic between browser and servers.
- **DNS:** Resolving domain names (openai.com → IP address).
- **TCP:** Reliable communication channel for web and application traffic.

## Observations
- HTTP packets contained GET and POST requests.
- DNS packets resolved multiple domains.
- TCP handled connection establishment using SYN, ACK flags.

## Conclusion
Wireshark successfully captured and displayed multiple network protocols, providing insights into packet-level communication.
