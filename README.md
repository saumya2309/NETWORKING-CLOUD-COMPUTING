# NETWORKING-CLOUD-COMPUTING

# TUN- 
It is a virtual network interface used to route IP packets in user space. It’s part of the TUN/TAP driver system in Unix-like operating systems:
- TUN simulates a layer 3 (IP) device.
- TAP simulates a layer 2 (Ethernet) device.
-  Use Cases of TUN in Cloud Environments

-  
- VPNs: TUN interfaces are commonly used to create encrypted tunnels between cloud servers and clients.
- Container Networking: Tools like Kubernetes or Docker may use TUN interfaces for overlay networks.
- Custom Routing: Developers can use TUN interfaces to intercept and manipulate IP traffic for advanced routing or firewall logic.
- Cloud Security: TUN interfaces help isolate traffic and enforce security policies across virtual machines or containers.

# Example: TUN in a VPN Setup
When you connect to a VPN hosted in the cloud:
- A TUN interface is created on your device.
- IP packets are routed through this interface.
- The VPN software encrypts and sends them to the cloud server.
- The server decrypts and forwards them to the destination.

- # TAP
- TAP (Terminal Access Point) is a mechanism that allows cloud administrators to mirror network traffic from virtual machines (VMs) or interfaces to monitoring tools. It’s especially useful for network visibility, security analysis, and performance diagnostics.

# OVS(Open Vswitch)
Open vSwitch (OVS) is a multilayer virtual switch designed to enable network automation and programmable control in virtualized environments. It is widely used in cloud platforms, data centers, and Software-Defined Networking (SDN) setups.
- Open-source: Licensed under Apache 2.0, making it freely available and customizable.
- Layer 2 and Layer 3 switching: Supports both data link and network layer operations.
- OpenFlow-capable: Integrates with SDN controllers for centralized network management.In cloud environments, especially those using virtual machines (VMs) or containers, networking must be flexible, scalable, and programmable.
-  OVS plays a key role by:
- Connecting VMs and containers within a host or across hosts.
- Enabling network virtualization by abstracting physical network hardware.
- Supporting automation through APIs and SDN protocols like OpenFlow.
- Enhancing performance with features like flow caching and kernel-space switching.

- # VXLAN
- VXLAN encapsulates Layer 2 Ethernet frames inside Layer 4 UDP packets, allowing virtual networks to span across physical boundaries. It’s a key enabler of overlay networking, which is essential in cloud environments where tenants need isolated networks across distributed infrastructure.
- Encapsulation protocol: Wraps Ethernet frames in UDP packets using port 4789 (or 8472 in older implementations).
- VXLAN Tunnel Endpoints (VTEPs): Devices (virtual or physical) that initiate and terminate VXLAN tunnels.

# IMPORTANCE
Traditional VLANs are limited to 4,096 IDs due to their 12-bit identifier. VXLAN solves this by using a 24-bit VXLAN Network Identifier (VNID), supporting up to 16 million logical networks.
Benefits:
- Massive scalability for large cloud deployments
- Tenant isolation in multi-tenant environments
- Layer 2 adjacency across Layer 3 boundaries
- Support for dynamic provisioning via SDN controllers

  
# FLANNEL
Flannel is a container networking solution that helps Kubernetes pods communicate across nodes. It creates an overlay network that assigns each host a unique subnet from a larger address space, allowing containers on different machines to talk as if they’re on the same local network.
- Developed by CoreOS, now maintained by the Flannel community.
- Works as a CNI (Container Network Interface) plugin for Kubernetes.
- Supports multiple backend mechanisms like VXLAN, host-gw, UDP, and AWS VPC.

# CLOUD NATIVE INTERFACE
CNI is a Cloud Native Computing Foundation (CNCF) project that defines a specification and libraries for configuring network interfaces in Linux and Windows containers. It focuses on:
- Connecting containers to networks
- Assigning IP addresses
- Cleaning up network resources when containers are deleted
CNI is written in Go and is designed to be simple, modular, and extensible, making it ideal for cloud-native platforms like Kubernetes.

# LIBVIRT
Libvirt provides a standardized interface for managing virtual machines (VMs), storage, and network resources across different hypervisors. It abstracts the complexity of underlying virtualization platforms and offers tools for automation, orchestration, and integration.
- Written in C, with bindings for Python, Go, and other languages
- Supports KVM/QEMU, Xen, VMware, Hyper-V, and Cloud Hypervisor
- Used by platforms like OpenStack, oVirt, and virt-manager

# ZERO COPY
Zero Copy refers to a data access paradigm where systems can use data directly from its original source—without duplicating, moving, or transforming it. This is especially relevant in cloud-native environments where data resides across multiple platforms (like Snowflake, Databricks, AWS S3, etc.).
Instead of traditional ETL (Extract, Transform, Load) pipelines that copy data into a centralized warehouse, Zero Copy enables in-place querying and real-time integration.

# OVERLAYS
An overlay network is a logical or virtual network that sits atop a physical (underlay) network. It abstracts the underlying infrastructure, allowing cloud platforms to create isolated, programmable, and dynamic networking environments.
- The underlay is the actual physical network (routers, switches, cables).
- The overlay is a virtual layer that uses tunneling protocols to connect endpoints across the underlay.

Cloud environments are multi-tenant, distributed, and dynamic. Overlay networks solve key challenges:
- Tenant isolation: Each user or application gets its own virtual network.
- Scalability: Supports millions of virtual networks using protocols like VXLAN.
- Flexibility: Works across hybrid and multi-cloud setups.
- Security: Enables encrypted tunnels and policy enforcement.


  


