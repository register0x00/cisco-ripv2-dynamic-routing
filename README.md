# Cisco RIPv2 Dynamic Routing Architecture

A multi-router Wide Area Network (WAN) simulation designed and configured in **Cisco Packet Tracer**. This project demonstrates the implementation of the dynamic routing protocol **RIPv2** across multiple autonomous network segments.

## 🌐 Network Topology
<img width="1920" height="1009" alt="2026-11-05_19-24-30" src="https://github.com/user-attachments/assets/43c227cb-8d83-4b99-a75e-9c9514334b38" />

### ⚙️ Technical Details & Infrastructure:
* **Multi-Router Chain:** Configured 3 **Router-2901** nodes simulating a path from a local SOHO infrastructure through an ISP backbone to a remote Web Server.
* **Dynamic Route Propagation:** Used **RIP version 2** to automatically build and update routing tables across all nodes without using static routes.
* **Separated Network Zones:**
  * Private LAN (Home): `192.168.1.0/24`
  * WAN Link 1 (Home to ISP): `10.0.0.0/24`
  * WAN Link 2 (ISP to Server Backbone): `20.0.0.0/24`
  * Remote Data Center LAN (Server): `192.168.2.0/24`
* **End-to-End Verification:** Successful ICMP pings and end-to-end data delivery verified from internal client machines to the public server node.

## 🛠️ Tools Used
* **Cisco Packet Tracer** (Simulation & configuration environment)
* **File format:** `.pkt`

## 🚀 How to Run & Verify
1. Download the `.pkt` file from this repository.
2. Open it in **Cisco Packet Tracer**.
3. Open the CLI on any router and type `show ip route` to analyze the dynamic routing table (look for the **R** marker).
4. Run a ping from `PC0` (Home) to `192.168.2.2` (Server) to test automated convergence.

