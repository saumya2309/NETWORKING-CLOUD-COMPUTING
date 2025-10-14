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

