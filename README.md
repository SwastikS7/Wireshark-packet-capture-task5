# Task 5 — Wireshark Packet Capture & Analysis

**Files included**
- `demo_anonymized_nopayload.pcap` — packet-captured pcap file
- `README.md` — this document
- `report.md` — short analysis report (see below)
- `screenshots/` — Wireshark screenshots (filters and interesting packets)

---

## Summary / Purpose

This repository contains an anonymized packet capture and supporting artifacts for **Task 5**.  
The original raw capture was processed to protect privacy and remove sensitive payload data before sharing publicly. The goals:

1. Demonstrate packet capture using Wireshark.
3. Provide a short analysis summary of the network traffic observed.

---

**Capture file:** `demo_anonymized_nopayload.pcap`

## 1. Protocols observed
- **DNS** — domain name resolution observed (queries & responses)
- **TCP** — multiple TCP flows (SYN / SYN-ACK / ACK)
- **HTTP / HTTPS** — HTTP metadata visible for some flows, HTTPS encrypted (no payload visible)

## 2. Observations
- Several TCP connections to remote servers established; TLS handshakes visible.
- No plaintext HTTP bodies or cookies visible after anonymization — payloads were stripped for privacy.

## 3. Conclusions / Learning points
- Packet captures are valuable for diagnosing network behavior and protocol flows.
- The provided capture preserves headers and flow relationships so graders can verify the observed protocols and packet patterns.

## 4. Commands used
- `tcp.port == <port>` for filtering packets with ports
