<img width="1318" height="684" alt="image" src="https://github.com/user-attachments/assets/214c12ad-3e1c-4623-a323-6a4f5c6f056d" />
# 🧠 Network Topology Overview

## 🌐 VLAN Configuration

| VLAN ID | Network Address   |
|----------|------------------|
| VLAN 10  | `192.168.10.0/24` |
| VLAN 20  | `192.168.20.0/24` |
| VLAN 30  | `192.168.30.0/24` |

---

## ⚙️ HSRP Configuration

- **Router 1** → Standby  
- **Router 2** → Backup  

> 🔁 Provides automatic failover and high availability between routers.

---

## 🌳 STP (Spanning Tree Protocol)

- **Enabled** on all VLANs  
- **Purpose:** Prevent Layer 2 loops  
- **Domain:** `DC`

---

## 🧭 Domain Controller & DNS Server

| Service | Hostname | IP Address | Description |
|----------|-----------|-------------|--------------|
| Domain Controller | `DC.local` | `192.168.0.2` | Central authentication & group policy |
| DNS Server | `192.168.0.2` | Same as DC | Internal name resolution for all VLANs |

---

## 🧩 Summary

- All VLANs are connected via trunk ports between switches and routers.  
- DHCP servers provide dynamic IPs for each VLAN scope.  
- HSRP ensures gateway redundancy.  
- STP maintains loop-free Layer 2 topology.  
- DNS & DC centralized at `192.168.0.2` for entire network domain.
