playbook: Deterministic Migration
version: 1.1
last_reviewed: 2026-08-03

**\>\_ SYSTEM MESSAGE: CURATED PATH LOADED.**

Architect,

You requested the **Deterministic Migration Playbook** - which tells me you are treating the Broadcom shift as an engineering correction, not a procurement exercise.

This path focuses on execution physics, control-plane abstraction, and the reality of translating workloads from legacy monolithic hypervisors to distributed HCI. The catalog has expanded significantly since this playbook was built. Three sections: the migration execution sequence, the decision and assessment layer, and architecture references plus tools.

**\>\_ SECTION 01: START HERE - MIGRATION EXECUTION SEQUENCE**

This path is sequenced. The strategic layer before the execution layer.

- [The Hypervisor Is Not the Migration Target — The Operating Model Is](https://www.rack2cloud.com/virtualization-operating-model-migration/) - Why treating the migration as a hypervisor swap instead of an operating model transition sets up the rest of the exit to fail
- [Broadcom Exit Strategy: The Post-Broadcom Migration Architecture](https://www.rack2cloud.com/post-broadcom-migration-architecture/) - Mapping the blast radius, Layer-2 network extensions, and IP continuity
- [The Architecture of Migration: Why Licensing Isn't Your Biggest Risk](https://www.rack2cloud.com/architecture-of-migration-licensing-risk/) - Why moving the VMDK is the last thing you should do and how scheduler physics change
- [VMware Licensing Pressure Created a Dependency Audit Problem](https://www.rack2cloud.com/vmware-dependency-audit/) - Why the exit decision forces a dependency audit before any workload can safely move
- [Beyond the VMDK: Translating Execution Physics from ESXi to AHV](https://www.rack2cloud.com/beyond-the-vmdk-translating-execution-physics-esxi-ahv/) - Why your ESXi performance model breaks on AHV and exactly how to rebuild it
- [Sizing for the CVM: The HCI Controller Tax](https://www.rack2cloud.com/controller-tax-hyperconverged-resource-contention/) - Calculating the hidden silicon overhead required to survive a workload spike and failure rebuild
- [Migration Stutter: Solving High-I/O Cutovers Without Data Loss](https://www.rack2cloud.com/migration-stutter-high-io-cutover/) - Fixing data gravity, write amplification, and high-latency cutovers
- [Policy Translation: Mapping VMware DRS, SRM & NSX to Nutanix Flow](https://www.rack2cloud.com/vmware-policy-migration-drs-srm-nsx-flow/) - Translating VMware policy constructs to AHV equivalents without losing enforcement fidelity
- [Upgrade Physics: Designing for Rolling Maintenance on AHV](https://www.rack2cloud.com/upgrade-physics-rolling-maintenance-ahv/) - Why most teams crash their first AHV upgrade cycle and how to sequence rolling maintenance without triggering upgrade storms
- [What Breaks First After You Leave VMware](https://www.rack2cloud.com/post-vmware-migration-what-breaks/) - The operational failures the migration dashboard never shows
- [The VMware Skills Gap Is the Real Exit Risk](https://www.rack2cloud.com/vmware-skills-gap-exit-risk/) - Why the hardest part of the exit isn't the technology
- [The Dashboard Said the Migration Succeeded](https://www.rack2cloud.com/migration-dashboard-failure/) - What the migration dashboard never shows and why "complete" isn't the same as "correct" (cross-reference; primary home is Virtualization Architecture Section 01)

**\>\_ SECTION 02: GO DEEPER - DECISION LAYER & PLATFORM ASSESSMENT**

Platform decisions, cost modeling, and the legal and licensing reality before you commit.

- [Nutanix vs VMware: The Post-Broadcom Decision Framework (2026)](https://www.rack2cloud.com/nutanix-vs-vmware-post-broadcom-decision-framework/) - Vendor exposure, migration physics, and conditional exit strategy
- [Nutanix vs VMware: Availability vs Authority in the Post-Broadcom Datacenter](https://www.rack2cloud.com/nutanix-vs-vmware-availability-authority/) - The control plane authority question that outlasts the licensing decision
- [Proxmox vs Nutanix vs VMware: The Post-Broadcom Constraints No One Explains](https://www.rack2cloud.com/proxmox-vs-nutanix-vs-vmware-post-broadcom/) - The operational constraints that don't appear in the vendor comparison matrix
- [The "Lift-and-Shift to KVM" Fallacy](https://www.rack2cloud.com/lift-and-shift-kvm-migration-fallacy/) - Why the easy path produces the most expensive Day-2 problems
- [VMware Licensing Costs: Why Most Estimates Are Wrong (And How to Fix Them)](https://www.rack2cloud.com/vmware-licensing-costs-estimate/) - The cost modeling failure that makes migrations look cheaper than they are until they aren't
- [The Broadcom Legal Playbook: Why the VMware Lawsuits Are Accelerating Enterprise Exit Timelines](https://www.rack2cloud.com/broadcom-vmware-lawsuit-legal-playbook/) - The legal pressure layer accelerating exit decisions independent of technical readiness
- [Proxmox vs VMware in 2026: A Migration Playbook That Actually Works](https://www.rack2cloud.com/proxmox-vs-vmware-migration-playbook-ve9/) - A durable migration methodology for teams evaluating Proxmox as the VMware exit target
- [Azure VMware Solution vs Native Azure: Architecture Trade-offs, Costs, and Exit Risk](https://www.rack2cloud.com/azure-vmware-solution-vs-native-azure/) - When AVS is a bridge and when it's a trap
- [Performance Modeling the VMware Evacuation: Nutanix AHV vs Proxmox Ceph Storage I/O Reality](https://www.rack2cloud.com/vmware-exit-performance-modeling-ahv-vs-ceph/) - Real I/O numbers before you commit to a target platform

**\>\_ EXTENDED PATH - KUBERNETES EXIT RAMP**

- [Kubernetes as the VMware Exit Ramp: How Platform Teams Are Reducing VMware Dependence](https://www.rack2cloud.com/kubernetes-vmware-exit-ramp/) - How VMware mental models break in Kubernetes and what to rebuild first

**\>\_ SECTION 03: ARCHITECTURE, TOOLS & DECISION FRAMEWORKS**

Pillar pages, learning paths, and tools to validate your environment before migration begins.

**Architecture References**

- [Virtualization Architecture - Pillar Hub](https://www.rack2cloud.com/virtualization-architecture/)
- [Nutanix AHV - Enterprise HCI](https://www.rack2cloud.com/virtualization-nutanix-ahv-architecture/)
- [VMware vSphere Legacy Ops](https://www.rack2cloud.com/virtualization-vmware-vsphere-esxi/)
- [The Broadcom Exit Strategy - Full Page](https://www.rack2cloud.com/post-broadcom-migration-architecture/)
- [Alternative Stacks - Open Source](https://www.rack2cloud.com/virtualization-alternative-hypervisors/)
- [Migration Strategy Architecture Path](https://www.rack2cloud.com/migration-strategy-learning-path/)
- [Modern Virtualization Learning Path](https://www.rack2cloud.com/modern-virtualization-learning-path/)
- [HCI Architecture Path](https://www.rack2cloud.com/hci-learning-path/)

**Decision Frameworks**

- [The CVM Tax: Why Mis-Sized VMs Kill AHV Performance](https://www.rack2cloud.com/cvm-tax-nutanix-ahv-performance/) - The invisible I/O penalty that surfaces after migration, not during it
- [The Nutanix Migration Stutter: Why AHV Cutovers Freeze High-IO Workloads](https://www.rack2cloud.com/nutanix-migration-stutter-ahv-fix/) - The final delta sync failure mode specific to Nutanix Move
- [The Repatriation Calculus: What the 93% Signal Actually Means](https://www.rack2cloud.com/cloud-repatriation-calculus/) - If AVS or cloud-first migration is on the table, run this math first

**Tools - Engineering Workbench**

- [VMware to HCI Migration Advisor](https://www.rack2cloud.com/vmware-to-hci-migration-advisor/) - Validate sizing and detect snapshot debt before hardware procurement
- [VMware Licensing Cost Model](https://www.rack2cloud.com/vmware-licensing-cost-model/) - Model the real renewal exposure before the exit conversation with leadership
- [VMware VVF & VCF Core Calculator](https://www.rack2cloud.com/vmware-vvf-vcf-core-calculator/) - VVF vs VCF licensing tier decision under the new Broadcom model
- [Rubrik Virtual Stack TCO Calculator](https://www.rack2cloud.com/rubrik-virtual-stack-tco-calculator/) - Data protection cost modeling across VMware, Nutanix, and Hyper-V

**Audit Service**

- [VMware Migration Readiness Assessment](https://www.rack2cloud.com/audits/migration-readiness-assessment/) - Vendor-agnostic review of your vSphere environment, Broadcom exposure, dependency audit, and AHV migration readiness scoped to your renewal window

**\>\_ THIS PATH IS UPDATED. BEGIN WITH SECTION 01.**

**\>\_ THE DISPATCH:** You have been provisioned access to The Dispatch - weekly architectural analysis, no marketing fluff.

**\>\_ NEXT TRANSMISSION: MONDAY @ 0800 EST.**

**\>\_ END TRANSMISSION.**

[](https://www.rack2cloud.com/)

[Rack2Cloud](https://www.rack2cloud.com/) _Kubernetes is an eventual-consistency engine. Stop treating it like a collection of VMs._