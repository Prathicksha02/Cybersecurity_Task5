# Task5

## Objective
The purpose of this task is to capture and analyze live network traffic using Wireshark, identify different types of protocols, and observe packet-level communication.

---

## Tools Used

1. **Wireshark** – Network packet analyzer
2. **Terminal (Kali Linux)**– For generating network traffic
3. **Browser**– For secure web traffic testing

---

## Steps I used

1. Run the following command in terminal:
   
   **sudo wireshark**
  
   Wireshark GUI launched successfully.
2. Choose **ethO**, the active wireless network interface showing traffic activity.

3. Started packet capture by double-clicking the interface.
4. Run  the below commands in a terminal window:

   ping -c 4 www.google.com
   
   Generated ping requests to test ICMP and DNS traffic.

   curl http://neverssl.com

   Accessed a plain HTTP website to generate web traffic.

   https://www.google.com

   This generated secure HTTPS/TLS traffic.
5. After sufficient traffic generation, stopped the capture using the red square button in Wireshark.
6. Apply Protocol Filters

Applied display filters one by one in Wireshark to isolate protocol-specific traffic:

+-----------+----------------+---------------------------------------------------------------+
| Protocol  | Filter Applied | Observations                                                  |
+-----------+----------------+---------------------------------------------------------------+
| DNS       | dns            | Domain lookup packets visible                                 |
+-----------+----------------+---------------------------------------------------------------+
| ICMP      | icmp           | Ping request and reply packets visible                        |
+-----------+----------------+---------------------------------------------------------------+
| HTTP      | http           | Unencrypted web traffic from neverssl.com visible             |
+-----------+----------------+---------------------------------------------------------------+
| TLS       | tls            | Encrypted HTTPS traffic visible after visiting google.com     |
+-----------+----------------+---------------------------------------------------------------+
| TCP       | tcp            | General transport-level packets for connections               |
+-----------+----------------+---------------------------------------------------------------+


7. Saved the capture as:
   
   mycapture.pcap

---

## Protocols Identified

1. DNS (Domain Name System)

   Translates domain names (e.g., www.google.com) to IP addresses.

   Observed DNS requests and responses to Google DNS servers.

2. ICMP (Internet Control Message Protocol)

   Used by ping to test connectivity.

   Observed Echo Requests and Echo Replies.

3. HTTP (HyperText Transfer Protocol)

   Unencrypted web traffic for website access.

   Observed GET requests to neverssl.com.

4. TLS (Transport Layer Security)

   Provides encryption for secure web traffic (HTTPS).

   Observed TLS handshake and encrypted application data during visit to https://www.google.com.

5. TCP (Transmission Control Protocol)

   Reliable transport layer protocol for connection establishment and data transfer.

   Observed SYN, ACK, and data packets.

---

## Screenshots

Screenshot is included here: Screenshot_task5

---

## Conclusion
Successfully captured and analyzed live network traffic using Wireshark.
Observed key protocols including DNS, ICMP, HTTP, TLS, and TCP.
The .pcap file and this report demonstrate protocol awareness and basic network traffic analysis skills.



