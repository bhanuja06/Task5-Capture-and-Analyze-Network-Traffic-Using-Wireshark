# Network Traffic Analysis Report

## Network Summary
- **Subnet**: 192.168.29.0/24  
- **Capture Duration**: 1 minute  
- **Primary Protocols**: UDP, ARP, IGMPv3, ICMPv6  

---

## Protocol Analysis

### UDP Traffic
| Source IP       | Destination IP | Port | Purpose    |
|-----------------|----------------|------|------------|
| 192.168.29.152 | 8.8.8.8        | 53   | DNS Query  |
| 192.168.29.171 | 224.0.0.251    | 5353 | mDNS       |

### ARP Activity
- 192.168.29.152 → Broadcast (Who has 192.168.29.1?)  
- 192.168.29.1 → 192.168.29.152 (ARP Reply)  

### IGMPv3 Multicast
Membership reports detected from:  
- 192.168.29.152  
- 192.168.29.171  
*(Possible video streaming or local service discovery)*  

### ICMPv6 Traffic
| Type                  | Source          | Destination      |
|-----------------------|-----------------|------------------|
| Neighbor Solicitation | fe80::[local]   | ff02::1:ff00:1   |
| Router Advertisement  | fe80::[router]  | ff02::1          |

---

## Detected Network Devices
- 192.168.29.1 (Gateway)  
- 192.168.29.152  
- 192.168.29.171  
- 224.0.0.251 (mDNS)  
- ff02::1 (IPv6 All-Nodes)  

---

## Key Observations
1. Standard ARP traffic for local network resolution.  
2. Active multicast participation (IGMPv3) suggesting media services.  
3. IPv6 neighbor discovery and router advertisements.  
4. DNS queries to external resolver (8.8.8.8).  
