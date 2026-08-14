playbook: Kubernetes Day 2
version: 1.1
last_reviewed: 2026-08-03

**\>\_ SYSTEM MESSAGE: CURATED PATH LOADED.**

Architect,

You requested the **Kubernetes Day 2 Diagnostic Playbook** - which tells me you are tired of debugging symptoms and ready to fix the actual system physics.

You are operating in production, where the real pain starts. This path is built around the four control loops that govern Kubernetes failure: Compute, Network, Storage, and Identity. The catalog has expanded significantly. Three sections: the core diagnostic sequence, the deeper failure modes and platform-specific patterns, and architecture references plus tools.

**\>\_ SECTION 01: START HERE - THE CORE DIAGNOSTIC SEQUENCE**

This path is sequenced. The mental model comes before the deep dives.

- [Kubernetes Day 2 Failures: 5 Real-World Incidents & The Metrics That Predict Them](https://www.rack2cloud.com/kubernetes-day-2-failures/) - Five failure signatures, five metrics, one post - the pattern recognition layer before the deep dives
- [The Rack2Cloud Method: A Strategic Guide to Kubernetes Day 2 Operations](https://www.rack2cloud.com/kubernetes-day-2-operations-guide-rack2cloud-method/) - The foundational mental model: 4 Intersecting Control Loops
- [Kubernetes ImagePullBackOff: It's Not the Registry (It's IAM)](https://www.rack2cloud.com/kubernetes-image-pull-back-off-iam-guide/) - The Identity Loop: debugging silent auth failures and token TTLs
- [Your Kubernetes Cluster Isn't Out of CPU - The Scheduler Is Stuck](https://www.rack2cloud.com/kubernetes-scheduler-stuck-cpu-fragmentation/) - The Compute Loop: fixing fragmentation, PDB deadlocks, and bin-packing failures
- [It's Not DNS (It's MTU): Debugging Kubernetes Ingress](https://www.rack2cloud.com/kubernetes-ingress-502-debug-mtu-dns/) - The Network Loop: unpacking the 5-layer lie of overlay networking
- [Storage Has Gravity: Debugging PVCs & AZ Lock-in](https://www.rack2cloud.com/kubernetes-pvc-stuck-volume-node-affinity/) - The Storage Loop: surviving the double scheduler and stateful constraints
- [Kubernetes Resource Requests vs Limits: The Scheduler Guarantees One Thing - The Kernel Enforces Another](https://www.rack2cloud.com/kubernetes-resource-requests-vs-limits/) - The two-layer model that produces OOMKills, CPU throttle, and QoS eviction surprises
- [VPA vs HPA: Why Most Teams Choose the Wrong Autoscaler](https://www.rack2cloud.com/vpa-vs-hpa-kubernetes/) - The autoscaling decision that intersects with QoS class, eviction risk, and ingress reload frequency

**\>\_ SECTION 02: GO DEEPER - PLATFORM FAILURE MODES & RUNTIME LAYER**

The infrastructure dependencies that Kubernetes failure post-mortems consistently miss.

- [etcd Is Your Kubernetes Database: What It Does, What Breaks, and What to Watch](https://www.rack2cloud.com/etcd-kubernetes-database/) - The control plane persistence layer - when etcd degrades, the entire cluster degrades with it
- [containerd in Production: 5 Day-2 Failure Patterns at High Pod Density](https://www.rack2cloud.com/containerd-in-production-day2-failure-patterns/) - Runtime-level failures that surface under churn, not under steady-state
- [containerd vs CRI-O: Memory Overhead at Scale - Real Node Density Limits](https://www.rack2cloud.com/containerd-vs-cri-o-memory-overhead-scale/) - The memory overhead model that belongs in your node sizing calculation at 100+ pods per node
- [Vertical Pod Autoscaler in Production: In-Place Resize Works - Until It Doesn't](https://www.rack2cloud.com/vertical-pod-autoscaler-in-place-resize-production/) - The Kubernetes 1.35 in-place resize reality check for stateful workloads
- [Your Monitoring Didn't Miss the Incident - It Was Never Designed to See It](https://www.rack2cloud.com/observability-vs-monitoring/) - The observability gap between infrastructure monitoring and control loop failure visibility
- [Ingress-NGINX Deprecation: What to Do Next (Four Paths, Four Failure Modes)](https://www.rack2cloud.com/ingress-nginx-deprecation-what-to-do/) - The forced migration decision and what each path costs operationally
- [Kubernetes Is Moving Past Ingress - Most Clusters Aren't](https://www.rack2cloud.com/kubernetes-ingress-gateway-api-migration/) - The architectural shift and where most clusters sit in the transition
- [Gateway API Is the Direction - Your Controller Choice Is the Risk](https://www.rack2cloud.com/gateway-api-kubernetes-controller-decision/) - NGINX vs Envoy reload behavior, HPA dependency, and the controller decision that outlasts the migration
- [Kubernetes Ingress to Gateway API Migration: How to Move Without Breaking Production](https://www.rack2cloud.com/migrate-ingress-to-gateway-api-production/) - The annotation audit, ingress2gateway 1.0 reality check, and side-by-side deployment pattern
- [Operating Gateway API in Production: What the Migration Guides Don't Cover](https://www.rack2cloud.com/operating-gateway-api-production/) - Where routing failures go invisible and how to instrument for the decision layer
- [Service Mesh vs eBPF in Kubernetes: Cilium vs Calico Networking Explained](https://www.rack2cloud.com/service-mesh-vs-ebpf-kubernetes-cilium-vs-calico/) - The network layer decision below the ingress controller
- [Velero Going CNCF Isn't About Backup - It's About Control](https://www.rack2cloud.com/velero-cncf-backup-control/) - What CNCF governance actually changes operationally and what it doesn't touch
- [Google Just Moved the Control Plane Boundary](https://www.rack2cloud.com/control-plane-boundary-kubernetes-scale/) - What GKE Autopilot signals about managed control plane trade-offs at scale
- [GKE IP Exhaustion 2026: The /24 Trap & Autopilot's Hidden Cost](https://www.rack2cloud.com/gke-pod-ip-exhaustion-vpc-triage/) - The VPC IP math that bites clusters after node count crosses a threshold

**\>\_ SECTION 03: ARCHITECTURE, TOOLS & DECISION FRAMEWORKS**

Pillar pages, sub-domains, learning paths, and tools to validate your cluster posture.

**Architecture References**

- [Cloud Native Architecture - Pillar Hub](https://www.rack2cloud.com/cloud-native/)
- [Kubernetes Cluster Orchestration](https://www.rack2cloud.com/cloud-native-kubernetes-cluster-orchestration/)
- [Container Security Architecture](https://www.rack2cloud.com/container-security-architecture-strategy-guide/)
- [Service Mesh Architecture](https://www.rack2cloud.com/service-mesh-architecture/)
- [Platform Engineering Architecture](https://www.rack2cloud.com/platform-engineering-architecture/)
- [Cloud Architecture Learning Path](https://www.rack2cloud.com/cloud-learning-path/)

**Decision Frameworks**

- [Kubernetes Is Not an LLM Security Boundary](https://www.rack2cloud.com/kubernetes-llm-security-boundary/) - The isolation model that fails when AI workloads gain tool access
- [Seccomp vs AppArmor: Which Actually Stops Container Breakouts?](https://www.rack2cloud.com/seccomp-vs-apparmor-container-breakout/) - The security boundary question below the orchestration layer
- [PersistentVolumes vs StorageClasses: When You Actually Need Each](https://www.rack2cloud.com/persistentvolume-vs-storageclass-kubernetes/) - The storage abstraction decision that determines scheduling behavior for stateful workloads
- [Kubernetes as the VMware Exit Ramp](https://www.rack2cloud.com/kubernetes-vmware-exit-ramp/) - How platform teams are using Kubernetes to reduce VMware dependency during exit

**Tools - Engineering Workbench**

- [Engineering Workbench](https://www.rack2cloud.com/deterministic-tools-for-a-non-deterministic-cloud/) - Full tool catalog - cluster sizing, cost modeling, drift auditing
- [Kubernetes Cost Density Calculator](https://www.rack2cloud.com/kubernetes-cost-density-calculator/) - Model cost and node density tradeoffs for your cluster

**Audit Service**

- [Recovery Readiness Assessment](https://www.rack2cloud.com/audits/recovery-readiness-assessment/) - If Velero is your Kubernetes backup strategy, this validates whether your restore dependencies are actually modeled

**\>\_ THIS PATH IS UPDATED. BEGIN WITH SECTION 01.**

**\>\_ THE DISPATCH:** You have been provisioned access to The Dispatch - weekly architectural analysis, no marketing fluff.

**\>\_ NEXT TRANSMISSION: MONDAY @ 0800 EST.**

**\>\_ END TRANSMISSION.**

[](https://www.rack2cloud.com/)

[Rack2Cloud](https://www.rack2cloud.com/) _Kubernetes is an eventual-consistency engine. Stop treating it like a collection of VMs._