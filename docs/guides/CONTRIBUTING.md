# **Cisco Packet Tracer Contribution Guide**

## **Contents**

- [**Cisco Packet Tracer Contribution Guide**](#cisco-packet-tracer-contribution-guide)
  - [**Contents**](#contents)
  - [🧩 **Project Structure**](#-project-structure)
  - [🔒 Managing Sensitive Files](#-managing-sensitive-files)
    - [`.env` Files](#env-files)
    - [Configuration Files](#configuration-files)
  - [**Setting Up the Development Environment**](#setting-up-the-development-environment)
    - [**Setting Network Variables**](#setting-network-variables)
  - [**Workflow**](#workflow)
    - [**Creating Branches**](#creating-branches)
  - [🔍 **Testing and Verification**](#-testing-and-verification)
    - [**Network Standards**](#network-standards)
    - [✅ **Packet Tracer Network Simulation**](#-packet-tracer-network-simulation)
  - [**Commit Messages**](#commit-messages)
  - [**Submitting Pull Requests**](#submitting-pull-requests)
  - [Code Review](#code-review)
  - [📂 Verifying the Pipeline in the Repository](#-verifying-the-pipeline-in-the-repository)
  - [**Documentation Contributions**](#documentation-contributions)

## 🧩 **Project Structure**

**network/**: Contains the main Packet Tracer network topology files.  
**config/**: Configuration files for different VLAN and routing protocols.  
**scripts/**: Scripts for automating network setup and configuration in Cisco Packet Tracer.  
**tests/**: Network simulation test cases and verification files.  

## 🔒 Managing Sensitive Files

### `.env` Files

- **Description**: The **`.env`** file may contain sensitive information related to the network configuration, such as usernames, passwords, and API keys for Cisco configurations.

- **Setup**: Create a **`.env`** file in the root of the project based on the **`.env-example.txt`** file. This file should contain any sensitive network credentials.

- **Important**: The **`.env`** file is in **`.gitignore`** to ensure it is not uploaded to the repository.

### Configuration Files

- **Description**: The configuration files define the network settings, such as VLANs, IP addresses, and routing protocols.

- **Example Files**: Use **`config-example.txt`** as a template to set up your network configurations.

## **Setting Up the Development Environment**

### **Setting Network Variables**

- **Network Topology**: Review the VLAN configuration and subnets provided for setting up switches, routers, and other network devices. Ensure IP addressing, subnetting, and routing protocols align with the project’s requirements.

  | VLAN | Department       | Subnet          | Core Router |
  |------|------------------|-----------------|-------------|
  | 10   | Administration   | 10.0.10.0/24    | CORE 1      |
  | 20   | Finance          | 10.0.20.0/24    | CORE 1      |
  | 30   | Human Resources  | 10.0.30.0/24    | CORE 1      |
  | 40   | Sales            | 10.0.40.0/24    | CORE 1      |
  | 50   | Engineering      | 10.0.50.0/24    | CORE 1      |
  | 60   | IT               | 10.0.60.0/24    | CORE 2      |
  | 70   | Guests           | 10.0.70.0/24    | CORE 2      |
  | 80   | Maintenance      | 10.0.80.0/24    | CORE 2      |
  | 90   | Security         | 10.0.90.0/24    | CORE 2      |
  | 100  | VoIP             | 10.0.100.0/24   | CORE 2      |

## **Workflow**

### **Creating Branches**

- This project uses the **GitFlow** workflow for structured development. Each contribution should follow this workflow:

1. **Fork the Repository**.
2. **Create a Branch** following the GitFlow conventions (e.g., `feature/vlan-setup`).
3. **Commit and Push** your changes.
4. **Submit a Pull Request** for review.

## 🔍 **Testing and Verification**

### **Network Standards**

- Ensure configurations follow Cisco best practices for VLAN, routing, and security.
- Adhere to IP addressing standards for consistency and avoid address conflicts.

### ✅ **Packet Tracer Network Simulation**

- **Testing Tools**: Cisco Packet Tracer simulations and network verification tools.
- **Network Verification**: Test all VLANs, subnets, and connectivity between devices.
  - Ensure that all departments in each VLAN can communicate within their subnet.
  - Verify inter-VLAN routing based on the core routers.
  - Validate security policies to ensure restricted access where applicable.

## **Commit Messages**

- Use clear and descriptive commit messages to document changes. For example:
  - `Add VLAN 10 configuration for Administration`
  - `Configure routing between VLAN 20 and VLAN 50`

## **Submitting Pull Requests**

- Include a description of the changes and link to any related issues or network topology documentation.

## Code Review

- Pull requests will be reviewed to ensure compliance with Cisco networking standards and project guidelines.

## 📂 Verifying the Pipeline in the Repository

1. **CI/CD Pipeline**: Check the **Actions** tab in GitHub to review the CI/CD status.
2. **View Logs**: Each pipeline step provides logs for network simulations and testing.

## **Documentation Contributions**

- Follow the same process for contributing to documentation. Describe changes to network topologies, configuration guides, or VLAN setups in your PR description.
