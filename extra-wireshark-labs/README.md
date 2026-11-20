<div align="center">

# 🦈 Extra Work: Wireshark Labs

### 5 SOC-style labs + a 17-challenge quiz · packet analysis like a real analyst

![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white)
![Labs](https://img.shields.io/badge/SOC_Labs-5-blue?style=for-the-badge)
![Quiz](https://img.shields.io/badge/Quiz-17_challenges-orange?style=for-the-badge)
![Redacted](https://img.shields.io/badge/Secrets-Redacted-red?style=for-the-badge)

*Capture 📡 → filter 🔍 → find the evidence 🕵️ → write the report 📝*

</div>

---

## 🧪 Part 1: SOC labs

| # | 🔬 Lab | 🎯 Focus | 🏆 Result | 🔗 |
|:-:|-------|---------|:--------:|:-:|
| 1 | 🕵️ **Follow TCP Stream** | Data hidden in an HTTP response | ![100](https://img.shields.io/badge/100%2F100-brightgreen) | [Open ➜](lab-01-follow-tcp-stream/) |
| 2 | 📞 **Catch the Call Scammer** | SIP/RTP analysis and VoIP call replay | ![100](https://img.shields.io/badge/100%2F100-brightgreen) | [Open ➜](lab-02-call-scammer/) |
| 3 | 🔑 **HTTP Plain Text Credentials** | Cleartext logins in HTTP POST | ![100](https://img.shields.io/badge/100%2F100-brightgreen) | [Open ➜](lab-03-http-credentials/) |
| 4 | 📡 **Packet Capture** | Live capture, DNS and TLS handshake | `<score>` | [Open ➜](lab-04-packet-capture/) |
| 5 | 🗃️ **PCAP Analysis** | DNS and TLS analysis of a captured session | `<score>` | [Open ➜](lab-05-pcap-analysis/) |

## 🧩 Part 2: Wireshark quiz

17 short challenges on filters, protocol fields and statistics, each with the task, the method, the filter and a screenshot. **[Open the quiz ➜](wireshark-quiz/)**

| 🏷️ Category | 🔍 Challenges | 🛠️ Key tools |
|------------|--------------|-------------|
| 📋 Protocol fields | SNI, reply sender, TTL | `tls.handshake.extensions_server_name`, IPv4 header |
| 🔢 Counting | Packets per host, DNS queries, port 80 | `ip.addr`, `ip.src`, `tcp.dstport` |
| 🕵️ Follow TCP Stream | Hidden words and codes | `http.request.uri == "..."` |
| 🤝 TCP handshake | SYN packets | `tcp.flags.syn == 1 && tcp.flags.ack == 0` |
| 🔓 Clear-text data | HTTP and FTP logins | `http.request.method == "POST"`, `ftp.request.command` |
| 📊 Statistics | Protocol Hierarchy, Conversations | Statistics menu |
| 🩺 Diagnosis | Retransmissions, RST | `tcp.analysis.retransmission`, `tcp.flags.reset == 1` |

---

## 🧰 Skills demonstrated

| 🔍 Analysis | 🌐 Protocols | 🛡️ Security mindset |
|:--|:--|:--|
| Display filters, coloring rules | HTTP, DNS, TLS | Spotting cleartext credentials |
| Follow TCP Stream | SIP, RTP | Information disclosure |
| Statistics menu | TCP, FTP, ICMP | IOC extraction and redaction |

---

## 🗂️ Folder map

```
extra-wireshark-labs/
├── 📄 README.md
├── 🕵️ lab-01-follow-tcp-stream/
├── 📞 lab-02-call-scammer/
├── 🔑 lab-03-http-credentials/
├── 📡 lab-04-packet-capture/
├── 🗃️ lab-05-pcap-analysis/
└── 🧩 wireshark-quiz/
```

## 📌 Notes

- 🔒 Codes, card numbers and credentials are **redacted** everywhere.
- 🚫 No PCAPs, audio files or answer keys are included.
- ⚖️ Only analyse traffic you are authorised to capture.

<div align="center">

⬅️ [Back to the main page](../README.md) · 🧪 [Core deliverable: Week 1 lab setup](../week-01-lab-setup/)

*Labs by [NetworkWalks](https://networkwalks.com/wireshark)*

</div>