# Network Traffic Analysis Report

## Overview
This report summarizes the findings from a Wireshark network traffic capture. The analysis focuses on identifying protocols, devices, and key activities within the 192.168.29.0/24 subnet during a 1-minute capture window.

## Key Findings
- **Primary Protocols**: UDP, ARP, IGMPv3, ICMPv6
- **Detected Devices**: 
  - 192.168.29.1 (Gateway)
  - 192.168.29.152
  - 192.168.29.171
  - 224.0.0.251 (mDNS)
  - ff02::1 (IPv6 All-Nodes)
- **Notable Activities**:
  - DNS queries to 8.8.8.8
  - ARP requests and replies
  - IGMPv3 multicast membership reports
  - ICMPv6 neighbor discovery and router advertisements

## Usage
Open the `report.md` file for a detailed breakdown of the network traffic analysis.
