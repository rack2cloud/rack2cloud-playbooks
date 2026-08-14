playbook: Virtualization Architecture
version: 1.2
last_reviewed: 2026-08-03

**\>\_ SYSTEM MESSAGE: CURATED PATH LOADED.**

Architect,

You are receiving this because you requested the **Virtualization Architecture Playbook** - which tells me one thing: you are not here for marketing diagrams. You are here for operational truth.

This path covers the full stack: the Day-2 realities of running AHV in production, the physics of migration failure, and the post-Broadcom decision framework for what comes next. The catalog has grown significantly. This path is updated to reflect it.

**\>\_ SECTION 01: START HERE - CORE READING PATH**

This sequence is ordered. Start at the top.

- [The Hypervisor Is Not the Migration Target — The Operating Model Is](https://www.rack2cloud.com/hypervisor-is-not-the-migration-target-operating-model/) - Why optimizing for technical migration metrics misses the point
- [The Day-2 Reality of Nutanix AHV: An Architectural Deep Dive](https://www.rack2cloud.com/nutanix-ahv-day-2-deep-dive-operations/) - Real operational physics of AHV in production
- [vSphere to AHV Migration Strategy: A Risk-Deterministic Framework](https://www.rack2cloud.com/vsphere-to-ahv-migration-strategy/) - How to plan cross-platform migrations without surprise outages
- [ZFS vs Ceph vs NVMe-oF: Choosing the Right Storage Backend](https://www.rack2cloud.com/zfs-vs-ceph-vs-nvme-of-architecture-guide/) - Storage bottlenecks under virtualization and why they matter
- [What Breaks First After You Leave VMware](https://www.rack2cloud.com/post-vmware-migration-what-breaks/) - The operational failures the migration dashboard doesn't show
- [Your VMware Exit Was Successful. The First Incident Will Tell You If That's True.](https://www.rack2cloud.com/vmware-exit-successful-first-incident/) - Tooling-declared success versus operational health
- [The VMware Skills Gap Is the Real Exit Risk](https://www.rack2cloud.com/vmware-skills-gap-exit-risk/) - Why the hardest part of the exit isn't the technology

**\>\_ SECTION 02: GO DEEPER - PHYSICS & FAILURE MODES**

For architects who need to understand the mechanics, not just the outcome.

- [Nutanix AHV Operations: What Changes After VMware Migration](https://www.rack2cloud.com/nutanix-ahv-operations-after-vmware/) - What actually changes operationally once you're running AHV
- [The CVM Tax: Why Mis-Sized VMs Kill AHV Performance](https://www.rack2cloud.com/cvm-tax-nutanix-ahv-performance/) - The invisible I/O penalty that doesn't show up in Prism
- [The Nutanix Migration Stutter: Why AHV Cutovers Freeze High-IO Workloads](https://www.rack2cloud.com/nutanix-migration-stutter-ahv-fix/) - The final delta sync failure mode and how to prevent it
- [The Dashboard Said the Migration Succeeded](https://www.rack2cloud.com/migration-dashboard-failure/) - When the tooling reports success and the workload disagrees
- [The VM That Survived the Migration But Lost Its Identity](https://www.rack2cloud.com/vmware-migration-issues-identity-gap/) - Identity and configuration drift the migration tooling won't flag
- [Beyond the VMDK: Translating Execution Physics from ESXi to AHV](https://www.rack2cloud.com/beyond-the-vmdk-translating-execution-physics-esxi-ahv/) - What actually changes at the scheduler level
- [VMware Policy Migration: Translating DRS, SRM, and NSX to Nutanix Flow](https://www.rack2cloud.com/vmware-policy-migration-drs-srm-nsx-flow/) - Policy intent doesn't port automatically - this is how you do it
- [Performance Modeling the VMware Evacuation: AHV vs Proxmox Ceph Storage I/O](https://www.rack2cloud.com/vmware-exit-performance-modeling-ahv-vs-ceph/) - Real I/O numbers before you commit to a migration path
- [CPU Ready vs. CPU Wait: Why Your Cluster Looks Fine but Feels Slow](https://www.rack2cloud.com/cpu-ready-vs-cpu-wait-why-your-cluster-looks-fine-but-feels-slow/) - Distinguishing scheduler contention signals before they read as production failures
- [Resource Pooling Physics: CPU Wait & Memory Ballooning](https://www.rack2cloud.com/resource-pooling-physics-cpu-wait-memory-ballooning/) - The contention mechanics that cause silent degradation
- [The Storage Handshake Is Dead: Why HCI Redefines the Rules](https://www.rack2cloud.com/architecture-hci-vs-3-tier-storage-handshake/) - How HCI breaks the assumptions of 3-tier storage handshakes
- [The Physics of Disconnected Cloud: Modeling Microbursts & Metro Risk](https://www.rack2cloud.com/physics-disconnected-cloud-microbursts-metro-risk/) - Modeling microburst and metro-distance risk under disconnected operation
- [The "Lift-and-Shift to KVM" Fallacy](https://www.rack2cloud.com/lift-and-shift-kvm-migration-fallacy/) - Why the easy path is usually the wrong one
- [Proxmox Isn't Replacing VMware. It's Replacing Assumptions.](https://www.rack2cloud.com/proxmox-migration-assumptions/) - The assumptions Proxmox migrations quietly break

**\>\_ SECTION 03: ARCHITECTURE, TOOLS & DECISION FRAMEWORKS**

Pillar pages, decision frameworks, and tools to validate your environment.

**Architecture References**

- [Virtualization Architecture - Pillar Hub](https://www.rack2cloud.com/virtualization-architecture/)
- [Nutanix AHV - Enterprise HCI](https://www.rack2cloud.com/virtualization-nutanix-ahv-architecture/)
- [VMware vSphere Legacy Ops](https://www.rack2cloud.com/virtualization-vmware-vsphere-esxi/)
- [The Broadcom Exit Strategy](https://www.rack2cloud.com/post-broadcom-migration-architecture/)
- [Alternative Stacks - Open Source](https://www.rack2cloud.com/virtualization-alternative-hypervisors/)
- [Modern Virtualization Learning Path](https://www.rack2cloud.com/modern-virtualization-learning-path/)
- [Migration Strategy Architecture Path](https://www.rack2cloud.com/migration-strategy-learning-path/)

**Decision Frameworks**

- [Nutanix vs VMware: The Post-Broadcom Decision Framework (2026)](https://www.rack2cloud.com/nutanix-vs-vmware-post-broadcom-decision-framework/)
- [Proxmox vs Nutanix vs VMware: The Post-Broadcom Constraints](https://www.rack2cloud.com/proxmox-vs-nutanix-vs-vmware-post-broadcom/)
- [The Architecture of Migration: Why Licensing Isn't Your Biggest Risk](https://www.rack2cloud.com/architecture-of-migration-licensing-risk/)
- [vSphere Lifecycle Management Is a Governance Problem — Not a Patching Problem](https://www.rack2cloud.com/vsphere-lifecycle-management-governance/)
- [The Hypervisor Is Becoming a Policy Enforcement Point](https://www.rack2cloud.com/hypervisor-policy-enforcement-governance/)

**Tools - Engineering Workbench**

- [VMware to HCI Migration Advisor](https://www.rack2cloud.com/vmware-to-hci-migration-advisor/) - Validate sizing before hardware procurement
- [VMware Licensing Cost Model](https://www.rack2cloud.com/vmware-licensing-cost-model/) - Model the real renewal exposure
- [VMware VVF & VCF Core Calculator](https://www.rack2cloud.com/vmware-vvf-vcf-core-calculator/) - VVF vs VCF licensing tier decision
- [Rubrik Virtual Stack TCO Calculator](https://www.rack2cloud.com/rubrik-virtual-stack-tco-calculator/) - Data protection costs across VMware, Nutanix, Hyper-V

**Audit Service**

- [VMware Migration Readiness Assessment](https://www.rack2cloud.com/audits/migration-readiness-assessment/) - Vendor-agnostic review of your vSphere environment, Broadcom exposure, and AHV migration readiness

**\>\_ THIS PATH IS UPDATED. BEGIN WITH SECTION 01.**

**\>\_ THE DISPATCH:** You have been provisioned access to The Dispatch - weekly architectural analysis, no marketing fluff.

**\>\_ NEXT TRANSMISSION: MONDAY @ 0800 EST.**

**\>\_ END TRANSMISSION.**

[](https://www.rack2cloud.com/)

[Rack2Cloud](https://www.rack2cloud.com/) _Operational truth > marketing fiction._