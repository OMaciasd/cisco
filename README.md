# 📋 Cisco Packet Tracer Network Project

This project implements a basic network topology using Cisco Packet Tracer. The topology organizes a network into multiple VLANs to support different departments within a hypothetical organization. The goal is to enhance network security and performance by logically segmenting network traffic and facilitating inter-departmental communication through appropriate routing and access control lists (ACLs).

## 🗂️ Table of Contents

- [📋 Cisco Packet Tracer Network Project](#-cisco-packet-tracer-network-project)
  - [📖 Project Description](#-project-description)
    - [🛑 Considerations](#-considerations)
    - [📂 Project Structure](#-project-structure)
  - [✅ Requirements](#-requirements)
  - [🔧 Installation and Setup](#-installation-and-setup)
  - [🚀 Running the Network Simulation](#-running-the-network-simulation)
  - [⚙️ Network Security](#️-network-security)
  - [🛠️ Technologies Used](#️-technologies-used)
  - [🏗️ Architecture](#️-architecture)
  - [🤝 Contributing](#-contributing)
  - [📜 License](#-license)

## 📖 Project Description

This project simulates a network environment within an organization, implementing VLANs (Virtual Local Area Networks) to segment traffic across different departments. Each VLAN represents a department with its own subnet, as described below:

| VLAN | Department         | Subnet           | Core Switch |
|------|---------------------|------------------|-------------|
| 10   | Administration      | 10.0.10.0/24     | 1           |
| 20   | Finance            | 10.0.20.0/24     | 1           |
| 30   | Human Resources    | 10.0.30.0/24     | 1           |
| 40   | Sales              | 10.0.40.0/24     | 1           |
| 50   | Engineering        | 10.0.50.0/24     | 1           |
| 60   | IT                 | 10.0.60.0/24     | 2           |
| 70   | Guest              | 10.0.70.0/24     | 2           |
| 80   | Maintenance        | 10.0.80.0/24     | 2           |
| 90   | Security           | 10.0.90.0/24     | 2           |
| 100  | VoIP               | 10.0.100.0/24    | 2           |

### 🛑 Considerations

- **Security**: ACLs are configured to restrict access between certain VLANs to ensure data privacy. For instance, sensitive departments like Finance and Human Resources have restricted access.
- **Inter-VLAN Routing**: Routers are configured to facilitate communication between departments where necessary.
- **Redundancy and Failover**: Core switches are set up to support failover for critical VLANs.

### 📂 Project Structure

```plaintext
.
├── PacketTracerFiles/
│   ├── CompanyTopology.pkt      # Packet Tracer project file with network topology
├── Documentation/
│   ├── NetworkDiagram.png       # Network architecture diagram
│   ├── VLAN_Config_Guide.md     # Detailed VLAN and ACL configuration instructions
└── README.md
```

## ✅ Requirements

- Cisco Packet Tracer 8.0 or later.
- Basic knowledge of networking, VLANs, and Cisco CLI commands.

## 🔧 Installation and Setup

1. Clone the repository to access the Packet Tracer file:

    ```bash
    git clone https://github.com/your-username/cisco-network-project.git
    cd cisco-network-project/
    ```

2. Open the `CompanyTopology.pkt` file in Cisco Packet Tracer to load the network simulation.

## 🚀 Running the Network Simulation

1. **Load the Topology**:
   - Open the `CompanyTopology.pkt` file in Cisco Packet Tracer.

2. **Test VLAN Connectivity**:
   - Use **Ping** to test connectivity within and across VLANs. For example:
     - Ping a device within the same VLAN (e.g., Administration).
     - Test inter-VLAN routing by pinging a device from a different VLAN, such as IT to Engineering.

3. **Apply ACLs**:
   - Navigate to the router or Layer 3 switch and apply ACLs to restrict or allow specific traffic flows as per the configuration in `VLAN_Config_Guide.md`.

## ⚙️ Network Security

In this network topology:
- **ACLs** (Access Control Lists) are implemented to restrict sensitive VLANs, like Finance and HR, from accessing non-essential resources.
- Separate **VLANs** for **Guest** and **VoIP** ensure guest users and voice traffic are isolated from critical business traffic.
- **Core Switches** are designated to ensure optimal routing paths and support failover mechanisms for high availability.

## 🛠️ Technologies Used

- **Cisco Packet Tracer**: Network simulation.
- **VLANs**: Network segmentation.
- **ACLs**: Traffic management and security.
- **Routing Protocols**: For inter-VLAN routing.

## 🏗️ Architecture

For detailed information on the network architecture and configuration guidelines, refer to the Network Diagram and the VLAN Config Guide, [Architecture Guide](./docs/guides/ARCHITECTURE.md)..

## 🤝 Contributing

To contribute, please review the Contribution Guide for setup instructions and best practices,  [Contribution Guide](./docs/guides/CONTRIBUTING.md).

## 📜 License

This project is licensed under the MIT License.
