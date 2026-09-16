# Microsoft-AZ-140-Azure-Virtual-Desktop-Specialty-Study-Guide
Practical Microsoft AZ-140 study guide covering Azure Virtual Desktop infrastructure, identity, security, FSLogix, apps, monitoring, automation, labs, and exam preparation.
# Microsoft AZ-140: Azure Virtual Desktop Specialty Study Guide

## Introduction

This repository is an independent study guide for the **Microsoft AZ-140: Configuring and Operating Microsoft Azure Virtual Desktop** exam.

It focuses on designing, deploying, securing, managing, monitoring, and maintaining Azure Virtual Desktop (AVD) environments, including session hosts, host pools, FSLogix, identity, applications, networking, automation, and disaster recovery.

The content follows Microsoft's current skills measured as of July 20, 2026. [1]

## Exam Overview

| Item | Information |
|---|---|
| Vendor | Microsoft |
| Certification | Microsoft Certified: Azure Virtual Desktop Specialty |
| Exam code | AZ-140 |
| Purpose | Validate skills for planning, delivering, managing, and monitoring Azure Virtual Desktop experiences and remote apps |
| Prerequisites | No formal prerequisite |
| Target role | Server/Desktop Administrator |
| Level | Intermediate |
| Exam duration | Verify current Microsoft scheduling information |
| Passing score | 700 or greater |
| Exam format | Microsoft certification exam; question count can vary |
| Certification renewal | Every 12 months |

Microsoft recommends experience with Azure compute, networking, identity, storage, resiliency, desktop environments, Azure portal, templates, scripting, and command-line tools. [1]

## Who Should Take It?

AZ-140 is designed for server or desktop administrators who design, implement, manage, and maintain Azure Virtual Desktop environments and remote applications.

Useful background includes:

- Azure administration
- Windows desktop administration
- Virtualization
- Networking
- Microsoft Entra ID
- Storage
- PowerShell
- Azure CLI
- Azure portal
- ARM templates or Bicep
- User and application management

## Exam Objectives / Domains

Microsoft's current skills measured are:

### 1. Plan and Implement an Azure Virtual Desktop Infrastructure — 40–45%

Study:

- AVD network capacity
- Session-host networking
- RDP Shortpath
- RDP Multipath
- QoS
- Azure Private Link
- Network troubleshooting
- FSLogix storage
- Azure Storage
- File shares
- Azure NetApp Files
- Host-pool architecture
- Session-host sizing
- OS and licensing selection
- Host pools and session hosts
- PowerShell
- Azure CLI
- ARM templates
- Bicep
- Session-host images
- Azure VM Image Builder
- Azure Compute Gallery
- Image lifecycle management

### 2. Plan and Implement Identity and Security — 15–20%

Understand:

- Active Directory Domain Services
- Microsoft Entra ID
- Microsoft Entra Domain Services
- Azure RBAC
- Conditional Access
- Passwordless authentication
- Smart cards
- Multifactor authentication
- Microsoft Entra single sign-on
- Microsoft Defender for Cloud
- Microsoft Defender Antivirus
- Microsoft Defender for Endpoint
- NSGs
- User-defined routes
- Azure Firewall
- Azure Bastion
- Just-in-time VM access
- App Control for Business
- Controlled Folder Access
- Trusted Launch
- Confidential VMs

### 3. Plan and Implement User Environments and Apps — 20–25%

Focus on:

- FSLogix Profile Containers
- FSLogix ODFC Containers
- FSLogix Cloud Cache
- Application masking
- AVD clients
- Device redirection
- Multimedia redirection
- Printing
- Universal Print
- Intune policies
- Group Policy
- RDP properties
- Session timeout
- Start VM on Connect
- Personal desktops
- Application groups
- RemoteApp
- Microsoft 365 Apps
- OneDrive
- Microsoft Teams
- Browser management
- App Attach
- Application packages

### 4. Monitor and Maintain an Azure Virtual Desktop Infrastructure — 10–15%

Study:

- AVD log collection
- Azure Monitor
- AVD Insights
- Workbooks
- Session monitoring
- Application-group management
- Host capacity
- Performance optimization
- Autoscaling
- Session-host updates
- Backup
- Disaster recovery
- Multi-region architecture
- FSLogix profile backup and restore
- Personal desktop backup
- Image backup

Microsoft's current exam guide provides the detailed objectives and notes that exam skills are periodically updated. [1]

## Detailed Study Notes

### Azure Virtual Desktop Architecture

Understand the relationship between:

**Azure Subscription → Host Pool → Session Hosts → Application Groups → Workspaces → Users**

Know the difference between:

- Personal host pools
- Pooled host pools
- Desktop application groups
- RemoteApp application groups

Choose architecture based on user requirements, isolation, scalability, and management.

### Host Pools and Session Hosts

Study:

- Session-host sizing
- VM SKU selection
- Operating-system selection
- User assignment
- Load-balancing behavior
- Session limits
- Host-pool settings
- Registration
- Scaling

Use automation through PowerShell, Azure CLI, ARM templates, or Bicep when repeatable deployments are required.

### Networking

Understand:

- Azure VNets
- Subnets
- NSGs
- User-defined routes
- Azure Firewall
- Private Link
- RDP Shortpath
- DNS
- Connectivity troubleshooting

RDP Shortpath can provide direct connectivity between supported endpoints and session hosts when the required network conditions are available.

### FSLogix

FSLogix is central to user-profile management in AVD.

Understand:

- Profile Containers
- ODFC Containers
- Cloud Cache
- Storage requirements
- Permissions
- Profile performance
- Profile recovery
- Application masking

A good design considers profile size, I/O performance, availability, network latency, and storage cost.

### Identity

Understand when to use:

- AD DS
- Microsoft Entra ID
- Microsoft Entra Domain Services

Study Azure RBAC, Conditional Access, MFA, SSO, and session-host permissions.

### Applications

Know different application-delivery approaches:

**Installed on image → Application Group/RemoteApp → App Attach**

Understand how Microsoft 365 Apps, OneDrive, Teams, browsers, and other applications behave in multi-session environments.

### Security

Use layered protection:

**Identity → Network → Session Host → Endpoint → Application → Monitoring**

Review Defender for Cloud, Defender for Endpoint, Defender Antivirus, Azure Firewall, NSGs, Bastion, JIT access, Trusted Launch, and security policies.

### Monitoring and Optimization

Use Azure Monitor and AVD Insights to analyze:

- Session performance
- Host health
- Resource utilization
- Connection issues
- User experience
- Capacity

Autoscaling should balance user demand, availability, performance, and cost.

## Important Concepts

Revise:

- Azure Virtual Desktop
- Host pools
- Session hosts
- Application groups
- Workspaces
- Personal desktops
- Pooled desktops
- FSLogix
- Profile Containers
- ODFC Containers
- Cloud Cache
- App Attach
- RDP Shortpath
- RDP Multipath
- Azure VNet
- NSGs
- Azure Firewall
- Private Link
- Microsoft Entra ID
- AD DS
- Conditional Access
- Azure RBAC
- MFA
- Microsoft Defender
- Azure Bastion
- Trusted Launch
- Azure Monitor
- AVD Insights
- Autoscaling
- Azure Compute Gallery
- Azure VM Image Builder
- PowerShell
- Azure CLI
- Bicep
- Disaster recovery
- Multi-region deployment

## Practical Examples / Labs

Use only Azure environments you are authorized to administer.

1. Create an Azure Virtual Desktop host pool.
2. Deploy session hosts using the Azure portal.
3. Create a custom session-host image.
4. Store an image in Azure Compute Gallery.
5. Automate session-host deployment with Bicep.
6. Configure a pooled host pool.
7. Configure a personal host pool.
8. Create desktop and RemoteApp application groups.
9. Configure Microsoft Entra authentication.
10. Implement Azure RBAC for AVD administration.
11. Configure NSGs and test connectivity.
12. Configure FSLogix Profile Containers.
13. Configure OneDrive and Microsoft 365 Apps for AVD.
14. Configure Teams optimization and test redirection.
15. Configure Azure Monitor and AVD Insights.
16. Test host-pool autoscaling.
17. Create a backup and recovery strategy.
18. Troubleshoot a deliberately misconfigured session host.

## Study Strategy

Use Microsoft Learn as the primary source.

Combine:

- AZ-140 study guide
- Microsoft Learn modules
- Azure Virtual Desktop documentation
- FSLogix documentation
- Hands-on Azure labs
- PowerShell practice
- Azure CLI practice
- Bicep deployment exercises
- AVD monitoring exercises
- Microsoft's official Practice Assessment

Microsoft specifically recommends training and hands-on experience before taking AZ-140. [1]

Prioritize scenario-based understanding: know **why** a particular host-pool, identity, storage, security, or monitoring configuration is appropriate.

## 30-Day Study Plan

**Days 1–4:** AVD architecture, host pools, session hosts, workspaces, and application groups.

**Days 5–8:** Networking, VNets, NSGs, routing, Private Link, RDP Shortpath, and troubleshooting.

**Days 9–12:** Session-host sizing, images, Azure Compute Gallery, VM Image Builder, PowerShell, CLI, and Bicep.

**Days 13–16:** Identity, Entra ID, AD DS, RBAC, Conditional Access, MFA, and SSO.

**Days 17–20:** Security, Defender, Azure Firewall, Bastion, JIT, Trusted Launch, and confidential VMs.

**Days 21–24:** FSLogix, user profiles, application delivery, Microsoft 365 Apps, OneDrive, Teams, and App Attach.

**Days 25–27:** Azure Monitor, AVD Insights, autoscaling, capacity, backup, and disaster recovery.

**Days 28–29:** Complete an end-to-end AVD deployment and troubleshoot common failures.

**Day 30:** Review weak areas, complete Microsoft's Practice Assessment, and verify the latest exam information.

## Common Mistakes

- Confusing host pools with application groups
- Ignoring session-host sizing
- Misconfiguring FSLogix storage permissions
- Choosing an identity model without considering requirements
- Treating all AVD networking as identical
- Ignoring RDP Shortpath requirements
- Deploying applications without considering multi-session behavior
- Forgetting Conditional Access and RBAC
- Ignoring image lifecycle management
- Monitoring hosts without monitoring user experience
- Using outdated AZ-140 objectives

## Exam-Day Tips

- Read each scenario completely.
- Identify whether the question is testing infrastructure, identity/security, user experience/apps, or monitoring.
- Pay attention to requirements such as cost, scalability, user experience, security, and management overhead.
- Eliminate configurations that do not satisfy a stated requirement.
- Know the difference between similar Azure services.
- Do not rely solely on memorized portal steps.
- Manage the available exam time carefully.
- Review flagged questions if time remains.
- Microsoft requires a score of 700 or greater to pass. [1]

## Final Checklist

- [ ] Understand AVD architecture
- [ ] Can design host pools
- [ ] Understand session-host sizing
- [ ] Comfortable with AVD networking
- [ ] Understand RDP Shortpath
- [ ] Can manage AVD images
- [ ] Comfortable with PowerShell, CLI, and Bicep
- [ ] Understand Entra ID and AD DS
- [ ] Understand RBAC and Conditional Access
- [ ] Can configure FSLogix
- [ ] Understand application groups and RemoteApp
- [ ] Understand Teams and OneDrive in AVD
- [ ] Can configure monitoring and autoscaling
- [ ] Understand backup and disaster recovery
- [ ] Completed hands-on AVD labs
- [ ] Reviewed Microsoft's current AZ-140 study guide
- [ ] Completed legitimate practice assessment

## Official Resources

- Microsoft Certified: Azure Virtual Desktop Specialty:
  https://learn.microsoft.com/credentials/certifications/azure-virtual-desktop-specialty/
- Official AZ-140 Study Guide:
  https://learn.microsoft.com/credentials/certifications/resources/study-guides/az-140
- Azure Virtual Desktop Documentation:
  https://learn.microsoft.com/azure/virtual-desktop/
- Microsoft Learn:
  https://learn.microsoft.com/training/
- FSLogix Documentation:
  https://learn.microsoft.com/fslogix/
- Azure Monitor:
  https://learn.microsoft.com/azure/azure-monitor/
- Azure Virtual Desktop Exam Readiness:
  https://learn.microsoft.com/shows/exam-readiness-zone/

Always verify Microsoft's current exam guide, skills measured, price, languages, delivery options, and certification policies before scheduling.

## Voucher / Discount

**Learn SecByte, an official Microsoft reseller partner**, provides certification voucher options and discounts where available.

Learn SecByte's official Black Friday offer provides up to 70% off selected Microsoft exam vouchers.

AZ-140 voucher:

https://learn.secbyte.org/vouchers/microsoft-az-140-d08t

Check the current offer and availability before purchasing. Do not assume the 70% promotion applies specifically to AZ-140 unless the current offer states that it does. Voucher pricing and availability may change.

## Disclaimer

This is an **independent/community study guide** and is not an official Microsoft certification document. Microsoft, Azure, Azure Virtual Desktop, Microsoft Entra, FSLogix, and related trademarks belong to Microsoft.

Candidates should verify current exam information, objectives, pricing, policies, and voucher availability directly with Microsoft.

This repository does **not** contain exam dumps, leaked questions, or recalled exam questions. It is intended for legitimate education, hands-on learning, and certification preparation only.
