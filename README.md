# Wireshark Packet Analysis (Linux)

## 📌 Objective
The goal of this task was to capture live network packets using **Wireshark** on Linux, analyze them, and identify different network protocols (DNS, TCP, HTTP, ICMP).

---

## 🛠️ Steps Performed
1. Installed Wireshark on Ubuntu using:
   ```bash
   sudo apt update
   sudo apt install wireshark -y

    Started Wireshark and selected the active interface (wlan0 for Wi-Fi).

    Generated traffic by:

        Running ping google.com (ICMP packets)

        Opening a website in browser (http://example.com) (HTTP packets)

        Performing DNS resolution automatically (DNS packets)

    Stopped the capture after ~1 minute.

    Applied filters (dns, tcp, http, icmp) to analyze packets.

    Exported the capture file as capture.pcapng.

🔍 Protocols Identified
1. DNS (Domain Name System)

    Observed DNS query and response when resolving google.com.

    Example:

        Query: Standard query for A record of google.com

        Response: IP address returned by DNS server

2. TCP (Transmission Control Protocol)

    Observed TCP three-way handshake:

        SYN → SYN, ACK → ACK

    Ensures reliable communication between client and server.

3. HTTP (Hypertext Transfer Protocol)

    Observed HTTP GET request when accessing example.com.

    Example:

        GET / HTTP/1.1

        Response: 200 OK

4. ICMP (Internet Control Message Protocol)

    Observed Echo request and Echo reply packets from the ping command.

    Example:

        Request: Echo (ping) request to google.com

        Reply: Echo reply from google.com

📸 Screenshots

All screenshots are available in the screenshots/ folder:

    interface_selection.png – Chosen interface for capture

    overall_packets.png – Unfiltered packet list

    dns_filter.png – DNS query/response

    tcp_handshake.png – TCP three-way handshake

    http_request.png – HTTP GET request

    icmp_ping.png – ICMP Echo request/reply

    export_capture.png – Exporting capture to .pcap

📁 Deliverables

    capture.pcap → Packet capture file

    README.md → This report

    /screenshots/ folder → Screenshots of captured packets and analysis

🎯 Key Learnings

    Understood how to capture live network traffic on Linux.

    Learned to filter and analyze different network protocols in Wireshark.

    Observed the working of DNS queries, TCP handshake, HTTP requests, and ICMP ping packets.

    Gained practical hands-on skills in packet analysis and protocol awareness.
