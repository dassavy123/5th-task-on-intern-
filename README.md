# 5th-task-on-intern-


🔎 Observations from the Capture

Interface: wlan0 (Wi-Fi interface).

Packets Counted: At least 862 packets captured, 0 dropped.

Protocols Seen:

UDP (highlighted rows in your screenshot).

TLS (Transport Layer Security, over TCP 443).

Ethernet II, IPv4, TCP are also visible in the packet dissection pane.

Key Packet Details (example from selected frame):

Frame size: 113 bytes captured.

Ethernet II:

Source MAC: 1e:ba:ec:ec:e0:e7

Destination MAC: c8:5e:a9:04:68:a7

IP Layer:

Source IP: 172.66.146.12

Destination IP: 192.168.60.226

Transport Layer:

Protocol: TCP

Src Port: 443 (HTTPS server)

Dst Port: 53204 (random client port)

Application Layer:

Transport Layer Security (TLS) handshake/data visible.

📑 Sample Report

Title: Wireshark Packet Capture Analysis (wlan0)

Date of Capture: 30-09-2025

Objective: To capture and analyze live traffic on the Wi-Fi interface and identify protocols involved.

1. Summary of Findings

During the one-minute capture on wlan0, a total of 862 packets were recorded. Analysis revealed the presence of multiple protocols including UDP, TCP, and TLS. The captured traffic indicates secure web browsing (HTTPS) and possibly other background communications. No packets were dropped, ensuring data integrity in the capture.

2. Protocols Identified

UDP: Used for quick, connectionless data transfer. Likely part of QUIC or DNS exchanges.

TCP (Port 443): Standard HTTPS connections.

TLS: Encrypted communication layered on TCP, confirming secure web traffic.

Ethernet II, IPv4: Underlying data link and network layer protocols.

3. Example Packet Analysis

Frame #861:

Source IP: 172.66.146.12 (public server, likely web server).

Destination IP: 192.168.60.226 (local client).

Ports: 443 → 53204 (HTTPS communication).

Protocol: TLS inside TCP.

Size: 648 bytes.

4. Conclusion

The capture shows a typical encrypted web browsing session over HTTPS.

DNS resolution likely occurred earlier (not visible in this frame set).

Secure TLS sessions were established between the client and remote server.

UDP packets suggest auxiliary services (possibly QUIC or DNS).

This demonstrates successful use of Wireshark to identify and analyze multiple layers of communication (Ethernet → IP → TCP/UDP → TLS).
