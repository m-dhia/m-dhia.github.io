---
title: The five nines concept
description: "Exploring the concept of 99.999%"
image: cover.webp
slug: five-nines-concept
date: 2023-12-27
categories:
    - Cybersecurity
tags:
    - Summary
---

## Introduction

###  What Does the Five Nines Mean?
Five nines signifies a system or service availability of 99.999%, with less than 5.26 minutes of downtime annually, whether planned or unplanned. Maintaining such high availability involves:
- Eliminate single points of failure
- Design for reliability
- Detect failures as they occur

However, achieving and sustaining this level of availability can be costly and resource-intensive. It often requires additional hardware purchases, leading to increased complexity in system configuration and higher risks of component failures.

 **Availability** | **Downtime per Year**
------- | --------
99% | 87 hours 36 mins
99.5% | 43 hours 48 mins
99.95% | 4 hours 23 mins
99.99% | 53 mins
99.999% | 5 mins

### Environments that Require Five Nines
While sustaining high availability can be costly, certain industries require "five nines" reliability:
- **Finance:** For continuous trading, compliance, and customer trust.
- **Healthcare:** To provide uninterrupted patient care.
- **Public Safety:** To ensure security and services.
- **Retail:** For efficient supply chains and customer satisfaction.
- **News Media:** To deliver real-time information to the public.

## Availability

### Threats to Availability
The following threats pose a high risk to data and information availability:
- Unauthorized access to the primary database
- Successful DoS attack
- Significant loss of confidential data
- Outage of mission-critical application
- Compromise of Admin or root user
- Detection of cross-site scripting or illegal file server share
- Website defacement affecting public relations
- Severe weather like hurricanes or tornadoes
- Catastrophic events like terrorist attacks or building fires
- Long-term utility/service provider outage
- Water damage from flooding or sprinkler failure

### Designing High Availability System
High availability incorporates three major principles to achieve the goal of uninterrupted access to data and services:

1. **Elimination or reduction of single-points of failure**:

It's crucial to address single points of failure, which can be central routers or switches, network services, or key IT staff. Any loss in these areas can severely disrupt the entire system. To mitigate this risk, it's important to implement processes, resources, and components that reduce these single points of failure. One effective strategy is to use high availability clusters, where a group of interconnected servers shares access to the same storage and network configurations. This setup allows all servers to handle services simultaneously, appearing as a single, resilient system. If one server fails, the others seamlessly continue processing without interruption.

2. **System Resiliency**:

System resiliency means maintaining data and operations even during attacks or disruptions. It involves redundant power and processing systems, so if one fails, the other can seamlessly take over without interruption. Resilience goes beyond just securing devices; it ensures that data and services remain available even under attack.

3. **Fault Tolerance**:

Fault tolerance allows a system to keep working even if one or more components fail. Data mirroring is an example, where a mirrored system provides uninterrupted service by supplying requested data if a fault occurs, like in a disk controller, without the user noticing any disruption.

## Measures to improve Availability

### Asset management

#### Asset Identification
Asset management, including a comprehensive inventory of hardware and software, is essential for determining configuration parameters. This inventory should cover all components susceptible to security risks:
- Hardware systems
- Operating systems
- Hardware network devices
- Network device operating systems
- Software applications
- Firmware
- Language runtime environments
- Individual libraries

Organizations can opt for automated solutions to track assets. Administrators should promptly investigate any configuration changes to ensure they are up-to-date and authorized.

#### Asset Classification
Asset classification groups an organization's resources based on shared traits. It should be applied to documents, data records, files, and disks. Critical informations requires the highest protection, possibly needing special handling.
An organization can use a labeling system based on information value, sensitivity, and criticality.
To identify and classify assets:
1. Define asset categories.
2. Assign owners to all assets and software.
3. Set classification criteria.
4. Implement the classification system.

#### Asset Standardization
Asset management oversees the lifecycle and inventory of technology assets like devices and software. In an IT asset management system, organizations define acceptable IT assets to align with their goals, reducing asset diversity. For instance, only compliant applications are installed. Eliminating non-compliant applications enhances security.
Asset standards specify the hardware and software products an organization supports. Quick action during failures ensures access and security. Without standardized hardware, personnel may struggle to find replacements, requiring more expertise and increasing maintenance costs in non-standard environments.

#### Risk Analysis
Risk analysis evaluates threats from natural and human-caused events to an organization's assets.
Asset identification aids in deciding which assets to safeguard. Risk analysis has four key goals:
- Identify assets and their value
- Identify vulnerabilities and threats
- Quantify the probability and impact of the identified threats
- Balance the impact of the threat against the cost of the countermeasure

**There are two approaches to risk analysis:**
1. **Quantitative Risk Analysis:**

It is a method that assigns numerical values to elements of the risk analysis process. It involves calculating the potential financial impact of a risk by considering factors like asset value, exposure factor (EF), annualized rate of occurrence (ARO), and annual loss expectancy (ALE). This approach provides management with concrete data to make informed decisions about risk mitigation and resource allocation.

2. **Qualitative Risk Analysis:**

It is a method that relies on subjective assessments and scenarios to evaluate risks. It involves a team evaluating each threat based on its likelihood and impact, usually plotted on a table. The results are used as a guide for decision-making, often focusing on threats within a specified risk zone. Unlike quantitative analysis, the numerical values in qualitative analysis are not directly proportional and are more subjective in nature.

#### Mitigation
Mitigation aims to lessen the impact or likelihood of a loss. Technical controls like authentication systems, file permissions, and firewalls are examples. It's crucial to balance the potential negative impact of mitigation measures with the benefits of risk reduction.
There are four common ways to reduce risk:
- Accept the risk and periodically re-assess
- Reduce the risk by implementing controls
- Avoid the risk by totally changing the approach
- Transfer the risk to a third party

In the short term, one strategy is to accept the risk and create contingency plans. Risk acceptance is a common practice for individuals and organizations. Modern methods reduce risk by incremental software development and regular updates to address vulnerabilities.
Risk transfer includes outsourcing, purchasing insurance, or maintenance contracts. Hiring specialists for critical tasks can reduce risk effectively. A good risk mitigation plan can include two or more strategies.

### Defense in Depth
Defense in depth, while not foolproof, helps organizations stay ahead of cyber threats by minimizing risk. Relying on a single defense leaves data vulnerable, so multiple layers of protection are crucial.

| Term       |
|:----------:|
| Layering   |
| Limiting   |
| Diversity  |
| Obscurity  |
| Simplicity |

#### Layering
A layered approach offers comprehensive security, as attackers must breach each layer, which becomes increasingly complex. Layering involves coordinating multiple defenses, like storing sensitive data in a server within a secured facility.

#### Limiting
Limiting data access minimizes threats. Access should be restricted to what's necessary for each user's role. For instance, the marketing team doesn't need payroll access.
Technology like file permissions helps, but procedure measures are also vital. Employees should be barred from taking sensitive documents off-site.

#### Diversity
For effective protection, layers of security must vary. If all layers are the same, breaching one means breaching all. Diverse layers make it harder for attackers. Each layer should use different techniques. Even if one layer is breached, the entire system remains secure.
To achieve diversity, organizations can use products from different companies for multifactor authentication. For instance, a server with sensitive data might require a swipe card from one company and biometric authentication from another.

#### Obscurity
Obscuring information safeguards data. Organizations should avoid disclosing details like server operating system versions or equipment types that cybercriminals could exploit. Error messages should also be generic to prevent revealing vulnerabilities. This concealment makes it harder for attackers to target a system.

#### Simplicity
Complexity doesn't always ensure security. Overly complex systems can be hard to manage and may even increase vulnerability. If employees struggle to configure them correctly, they can become easy targets for cybercriminals. A good security solution is simple internally but presents a complex front to deter attacks.

### Redundancy

#### Single Points of Failure
A single point of failure is a crucial part of an organization's operations that, if it fails, can halt other operations dependent on it. This can be hardware, a process, data, or a utility. Single points of failure are weak links that disrupt operations. The solution is to modify the critical operation to remove reliance on a single element or to introduce redundant components that can take over if a point fails.

#### N+1 Redundancy
N+1 redundancy is a system design principle where critical components (N) have at least one backup component (+1) to ensure system availability in case of failure. For example, in a data center, N+1 redundancy means the system can continue operating if one of its components, such as servers, power supplies, switches, or routers, fails. The +1 represents the additional backup component or system ready to take over if needed. While N+1 redundancy provides backup components, it does not create a fully redundant system.

#### RAID
RAID (Redundant Array of Independent Disks) combines multiple physical hard drives into a single logical unit for data redundancy and performance improvement. It spreads data across drives, so if one disk fails, data can be recovered from the others. RAID also speeds up data retrieval by using multiple drives. There are hardware-based and software-based RAID solutions, with the former requiring a specialized hardware controller. RAID uses different methods to store data across disks:
- **Parity**: Detects data errors.
- **Striping**: Writes data across multiple drives.
- **Mirroring**: Stores duplicate data on a second drive.

#### Spanning Tree
Spanning Tree Protocol (STP) is a network protocol that prevents loops in a network's topology when switches are interconnected via multiple paths. Its primary function is to ensure that redundant physical links between switches are loop-free, allowing only one logical path between all network destinations. STP achieves this by intentionally blocking redundant paths that could cause loops, while still maintaining them for redundancy. When a network cable or switch fails, STP recalculates the paths and unblocks the necessary ports to activate the redundant path, ensuring network availability.

#### Router Redundancy
The default gateway, usually a router, provides access to the network or the Internet. Relying on a single router as the default gateway poses a single point of failure. To mitigate this, organizations can set up a standby router. In a redundancy setup, routers use a protocol to determine which one forwards traffic. Each router has a physical and a virtual IP address; end devices use the virtual IP as the default gateway. Routers exchange periodic messages using their physical IPs to check availability. If the standby router stops receiving these messages from the forwarding router, it takes over. This ability to recover from gateway failures is called first-hop redundancy.

The list below outlines router redundancy options based on the communication protocol between network devices.
- **Hot Standby Router Protocol (HSRP):** HSRP ensures high network availability by providing first-hop routing redundancy. A group of routers uses HSRP to select an active device and a standby device. The active device routes packets, while the standby device takes over if the active one fails.
- **Virtual Router Redundancy Protocol (VRRP):** VRRP routers run the VRRP protocol with one or more routers on a LAN. In this setup, one router is elected as the virtual router master, and the others act as backups in case the master fails.
- **Gateway Load Balancing Protocol (GLBP):** GLBP protects data traffic from a failed router or circuit like HSRP and VRRP do, while also enabling load balancing between a group of redundant routers.

#### Location Redundancy
An organization may need to consider location redundancy depending on its needs. The following outlines three forms of location redundancy.
1. **Synchronous:**
   - Real-time synchronization.
   - Requires high bandwidth.
   - Locations must be close to reduce latency.

2. **Asynchronous Replication:**
   - Not real-time synchronized but close.
   - Requires less bandwidth.
   - Sites can be further apart due to reduced latency concerns.

3. **Point-in-time Replication:**
   - Periodic updates for backup data.
   - Most bandwidth conservative, no constant connection needed.

### System Reliance

#### Resilient Design
Resiliency involves methods and configurations to tolerate system or network failures. For instance, redundant links in a network using STP provide alternate paths in case of link failures, but switchover may not be immediate without optimal configuration.
Routing protocols also enhance resiliency, with fine-tuning improving switchover times. Testing non-default settings in a controlled environment can help optimize network recovery.
Resilient design goes beyond redundancy, requiring an understanding of business needs to create a truly resilient network.

#### Application Resilience
Application resilience refers to an application's ability to function despite component issues. Downtime can result from application errors, infrastructure failures, or planned maintenance. Achieving high availability in applications involves balancing infrastructure costs with potential business losses due to failures. The complexity and cost of solutions for application resilience increase with higher availability factors.

#### IOS Resilience
The Interwork Operating System (IOS) for Cisco routers and switches includes a resilient configuration feature for faster recovery from malicious or unintentional data loss. It maintains a secure working copy of the IOS image file and running configuration, preventing their removal. These secure files, known as the primary bootset, ensure system integrity.
 >The command underneath is used to protect the Cisco IOS image file from unauthorized modifications:
```cisco
secure boot-image
```

## Incident Response

### Incident response phases

#### Preparation
Incident response involves an organization's procedures following an event outside the normal range, such as a data breach that exposes sensitive information to an untrusted environment. This breach can result from accidental or intentional acts. To address incidents, organizations need an incident response plan and a Computer Security Incident Response Team (CSIRT) to manage the response. The team performs the following functions:
- Maintains the incident response plan
- Ensures its members are knowledgeable about the plan
- Tests the plan
- Gets management’s approval of the plan
The CSIRT can be a formal team within the organization or an ad hoc one. It follows predefined steps to ensure a uniform approach and completeness. National CSIRTs handle incident response at a country level.

#### Detection and Analysis
Detection begins when an incident is discovered. While organizations may invest in advanced detection systems, their effectiveness relies on administrators reviewing logs and monitoring alerts. Proper detection involves understanding the incident's cause, the data and systems affected, and promptly notifying senior management and relevant managers for remediation.
Detection and analysis includes the following:
- Alerts and notifications
- Monitoring and follow-up
Incident analysis identifies the source, extent, impact, and details of a data breach. Depending on the situation, the organization may decide to bring in forensic experts for further investigation.

#### Containment and Eradication, and Recovery
Containment involves immediate actions like disconnecting systems to stop information leaks. After identifying a breach, the organization must contain and eradicate it, which may require additional system downtime. Recovery involves resolving the breach and restoring systems to their pre-breach state.

#### Post-Incident Follow-Up
After returning to normal operations, the organization should investigate the incident by asking:
- What actions will prevent the incident from reoccurring?
- What preventive measures need strengthening?
- How can it improve system monitoring?
- How can it minimize downtime during the containment, eradication, and recovery phases?
- How can management minimize the impact to the business?
Reviewing lessons learned can help the organization improve its incident response plan.

### Incident response Technologies

#### Network Admission Control
Network Admission Control (NAC) ensures that only authorized users with compliant systems can access the network. It evaluates incoming devices against network policies, quarantines non-compliant systems, and manages their remediation. This can be achieved using existing network infrastructure and third-party software, or through a dedicated NAC appliance that controls access, evaluates compliance, and enforces security policies for all endpoints.
Common NAC systems checks include:
1. Updated virus detection
2. Operating systems patches and updates
3. Complex password enforcement

#### Intrusion Detection Systems
Intrusion Detection Systems (IDSs) passively monitor network traffic by copying it for analysis . Working offline, it compares the captured traffic with known malicious signatures, similar to how antivirus software checks for viruses.
Working offline means several things:
- IDS works passively
- IDS device is physically positioned in the network so that traffic must be mirrored in order to reach it
- Network traffic does not pass through the IDS unless it is mirrored
In passive mode, an IDS monitors and reports on traffic without taking any action. This is known as operating in promiscuous mode.
Operating with a copy of the traffic allows the IDS to monitor without affecting the packet flow, but it can't stop single-packet attacks. IDS often needs assistance from routers and firewalls to respond to attacks.
A more effective solution is to use an Intrusion Prevention System (IPS) that can detect and stop attacks in real time.

#### Intrusion Prevention Systems
An Intrusion Prevention System (IPS) operates in inline mode, meaning all traffic passes through it for analysis. It can immediately detect and address network issues, including sophisticated attacks, by analyzing packet contents and payloads. Unlike an Intrusion Detection System (IDS), an IPS does not allow malicious traffic to pass through. However, a misconfigured IPS can disrupt normal traffic flow.

#### NetFlow and IPFIX
NetFlow is a Cisco technology that gathers packet statistics from routers and switches. It's the standard for collecting network operational data. IP Flow Information Export (IPFIX) is based on NetFlow Version 9 and is used to export traffic flow information from routers to data collection devices. This data helps optimize network performance when used by network managers and applications that support the protocol.
Applications that support IPFIX can display statistics from routers that use the standard. Collecting, storing, and analyzing data from IPFIX-supported devices offers several benefits:
- Secures the network against internal and external threats
- Troubleshoots network failures quickly and precisely
- Analyzes network flows for capacity planning

#### Advanced Threat Intelligence
Advanced threat intelligence can help organizations detect cyberattacks at various stages, sometimes even before they occur, with the right information.
Organizations can detect attack indicators in their logs and system reports for the following security alerts:
- Account lockouts
- All database events
- Asset creation and deletion
- Configuration modification to systems
Advanced threat intelligence, consisting of event or profile data, enhances security monitoring and response. Understanding malware tactics is crucial as cybercriminals become more sophisticated. Improved visibility into attack methods allows organizations to respond faster to incidents.

## Disaster Recovery

### Disaster Recovery Planning

#### Types of Disasters
Maintaining organizational function during a disaster is critical. Disasters encompass natural or human-caused events that damage assets and hinder operations.

##### Natural Disasters
Natural disasters vary by location and can be challenging to predict. They generally fall into  the following categories:
- Geological disasters: earthquakes, landslides, volcanoes, tsunamis
- Meteorological disasters: hurricanes, tornadoes, snow storms, lightning, hail
- Health disasters: widespread illnesses, quarantines, pandemics
- Miscellaneous disasters: fires, floods, solar storms, avalanches

##### Human-caused Disasters
Human-caused disasters involve people or organizations and fall into the following categories:
- Labor events: strikes, walkouts, slowdowns
- Social-political events: vandalism, blockades, protests, sabotage, terrorism, war
- Materials events: hazardous spills, fires
- Utilities disruptions: power failures, communication outages, fuel shortages, radioactive fallout

#### Disaster Recovery Plan
During an ongoing disaster, the organization implements its Disaster Recovery Plan (DRP) to swiftly restore critical systems, including assessing, salvaging, repairing, and restoring damaged facilities and assets.
To create the DRP, answer the following questions:
- Who is responsible for this process?
- What does the individual need to perform the process?
- Where does the individual perform this process?
- What is the process?
- Why is the process critical?
A DRP must prioritize critical processes within the organization. When recovering, the organization focuses on restoring its mission-critical systems first.

#### Implementing Disaster Recovery Controls
Disaster recovery controls reduce the impact of a disaster, ensuring resources and business processes can quickly resume operations.
There are three types of IT disaster recovery controls:
- Preventative measures prevent disasters by identifying risks.
- Detective measures discover unwanted events, uncovering new threats.
- Corrective measures restore systems after disasters or events.

### Business Continuity Planning

#### Need for Business Continuity
Business continuity is crucial in computer security. While companies strive to prevent disasters and data loss, it's impossible to predict every scenario. Having plans for business continuity is vital. This plan, broader than a DRP, involves relocating critical systems while the original facility is repaired. Personnel adapt to alternative methods until normal operations resume.
Availability ensures that resources necessary for the organization remain accessible to personnel and systems.

#### Business Continuity Considerations
Business continuity controls are more than data backups and redundant hardware. They also rely on properly trained employees to configure and operate systems effectively. Data can be useless until it provides information. An organization should look at the following:
- Getting the right people to the right places
- Documenting configurations
- Establishing alternate communications channels for both voice and data
- Providing power
- Identifying all dependencies for applications and processes so that they are properly understood
- Understanding how to carry out automated tasks manually

#### Business Continuity Best Practices
The National Institute of Standards and Technology (NIST) developed the following best practices:
1. Write a policy that provides guidance for developing the business continuity plan and assigns roles for task execution.
2. Identify critical systems and processes and prioritize them based on necessity.
3. Identify vulnerabilities, threats, and calculate risks.
4. Identify and implement controls and countermeasures to reduce risk.
5. Devise methods to quickly restore critical systems.
6. Write procedures to maintain organizational functionality during chaos.
7. Test the plan.
8. Regularly update the plan.
