# Cisco Packet Tracer Network Infrastructure Project

## Project Overview

This project demonstrates the design and testing of a simulated network infrastructure using Cisco Packet Tracer. The network represents three departments — IT, Sales and HR — connected through a router and departmental switches, with an additional server on the IT network.

The project explores network topology design, IP addressing, DHCP configuration, HTTP server access and connectivity testing. Screenshots document the configuration process, successful tests and troubleshooting issues encountered.

## Project Objectives

- Design a network topology connecting IT, Sales and HR departments.
- Configure a server with a static IPv4 address.
- Explore automatic IP configuration using DHCP.
- Test connectivity between devices and departmental networks.
- Test access to a website hosted on the IT server.
- Investigate DHCP and network connectivity failures.
- Document test results and supporting evidence.

## Tools & Technologies

- **Network simulation:** Cisco Packet Tracer
- **Network devices:** Router, switches, PCs and server
- **Networking concepts:** IPv4 addressing, subnet masks, default gateways and DNS
- **Network services:** DHCP and HTTP
- **Testing:** Ping and client IP configuration checks
- **Documentation:** Screenshots and project report

## Network Topology

The simulated network contains:

- 1 router
- 3 departmental switches
- 6 PCs
- 1 server
- 3 departments: IT, Sales and HR

Each department has two PCs connected through its departmental switch. The router connects the departmental networks, while the server is located on the IT network.

This design provides a practical environment for exploring departmental network segmentation, addressing and connectivity.

## IP Addressing & Server Configuration

The IT server is configured with a static IPv4 address so that clients have a predictable destination for accessing its services.

| Setting | Configuration |
|---|---|
| Server IPv4 address | `192.168.10.2` |
| Subnet mask | `255.255.255.0` |
| Default gateway | `192.168.10.1` |
| DNS server shown in the IT DHCP lease | `192.168.10.2` |

The project uses the `192.168.10.x`, `192.168.20.x` and `192.168.30.x` address ranges in its IT, Sales and HR connectivity tests.

## Project Implementation & Testing

### 1. Network Topology Design

I created a simulated network containing a router, three departmental switches, six PCs and an IT server.

**What this demonstrates:**
- Connecting network devices in a simulated environment.
- Organising devices by department.
- Establishing a foundation for testing communication between networks.

### 2. Static IP Configuration on the IT Server

I configured the server with the IPv4 address `192.168.10.2`, subnet mask `255.255.255.0` and default gateway `192.168.10.1`.

**Why this matters:** A server hosting network services commonly benefits from a predictable IP address, making it easier for clients to reach the service.

### 3. Client IP Configuration and DHCP

I inspected client IP configuration screens and tested DHCP address assignment.

An IT PC successfully received the following settings:

| Setting | Observed value |
|---|---|
| IPv4 address | `192.168.10.6` |
| Subnet mask | `255.255.255.0` |
| Default gateway | `192.168.10.1` |
| DNS server | `192.168.10.2` |

This is evidence of a successful DHCP lease for the IT client.

The report also includes screenshots of failed DHCP requests from an earlier troubleshooting stage. These are retained as evidence of the problem encountered, not as proof that DHCP was working on every client or department.

### 4. HTTP Website Testing

I tested access to the website hosted on the IT server by opening the following address in a client browser:

```text
http://192.168.10.2
```

The browser displayed the **NETCORE SYSTEMS** website.

**Result:** The website was reachable from the test PC, demonstrating that the HTTP page hosted at the server address could be accessed during the test.

### 5. Network Connectivity Testing

I used ping tests to examine connectivity to addresses in the IT, Sales and HR network ranges.

The report records both successful and unsuccessful attempts.

One documented test showed that the HR address `192.168.30.5` responded successfully:

- Packets received: 4
- Packet loss: 0%

Another test from Sales to the IT address `192.168.10.5` returned:

```text
Destination host unreachable
```

The error was reported by `192.168.20.1`.

**Interpretation:** The results demonstrate that some tested communication succeeded while another attempt failed. A failed ping can have several causes, so further investigation of routing, device configuration and access control rules is required before attributing the result to a particular ACL.

## Results Summary

| Area | Observed result |
|---|---|
| Network topology | Router, three switches, six PCs and one server documented |
| IT server addressing | Static IPv4 configuration documented |
| IT client DHCP | Successful lease documented for `192.168.10.6` |
| DHCP troubleshooting | Earlier failed requests documented |
| HTTP testing | NETCORE SYSTEMS website reachable at `http://192.168.10.2` |
| HR connectivity | Four successful ping replies from `192.168.30.5` |
| Sales-to-IT connectivity | `Destination host unreachable` reported by `192.168.20.1` |
| ACL validation | Full configuration and rule-level cause not independently verified |
| FTP testing | Successful operation not demonstrated in the supplied report |

## Evidence & Screenshots

The accompanying project report includes screenshots documenting:

1. Overall network topology — report page 3.
2. IT server static IP configuration — report page 5.
3. Client IP configuration checks — report pages 6–7.
4. Successful IT client DHCP lease — report page 8.
5. DHCP request failure and troubleshooting — report pages 9–10.
6. HTTP website test — report page 12.
7. Client ping tests — report page 13.
8. HR reachability and Sales-to-IT ping result — report page 14.

The screenshots provide evidence of the network design, configuration screens and observed test results.

## Skills Developed

Through this project, I practised:

- Network topology design and device connectivity.
- IPv4 addressing and subnet mask configuration.
- Understanding default gateways and DNS settings.
- DHCP configuration checks and troubleshooting.
- HTTP service access testing.
- Ping-based connectivity testing.
- Interpreting network errors and investigating possible causes.
- Documenting configurations, results and troubleshooting evidence.

## Security & GRC Relevance

This project supports my development in networking, cybersecurity and Governance, Risk and Compliance (GRC).

Understanding network segmentation and access controls is important when assessing whether systems are appropriately separated and whether communication restrictions work as intended.

The project also reinforces the importance of collecting evidence, validating controls and documenting unsuccessful tests rather than assuming a security control is effective without sufficient proof.

## Limitations & Further Work

The supplied report does not establish that every configuration or service requirement has been completed successfully.

Potential next steps include:

- Investigating and resolving the remaining DHCP failures.
- Verifying IP addressing and connectivity across all six PCs.
- Reviewing router interfaces and routing configuration.
- Inspecting the complete ACL configuration and testing its intended rules.
- Confirming that Sales-to-IT restrictions are caused by the intended security policy rather than another configuration issue.
- Testing FTP separately if it is part of the project requirements.
- Capturing updated screenshots after outstanding checks are completed.

## Author

**Stephen Adesina**

Cybersecurity | Network Security | Information Security | GRC

This project forms part of my practical portfolio as I develop my networking, cybersecurity and security assurance skills.

