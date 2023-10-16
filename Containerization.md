___
# CONTAINERIZATION
Links: [[Programming]]
Status: #🌞 
Tags: [[Operating Systems]]

<!--- Created on: 2023.10.12, 09:06 --->

- ...
___

# Properties
Deployable: shipping code from one machine to another
Self-contained: Executable with required dependencies
Host-agnostic: Running in isolation of host machine
Can be built for multiple architectures (amd64, arm64)

# Docker vs. Kubernetes
-  Docker focuses on creating and running containers 
- Kubernetes handles container orchestration, scaling, load balancing, and service discovery





- based on linux features such as namespaces, cgroups, union file systems
![[Pasted image 20231012093347.png]]
- registry: store static images
- Images: static, persistent container??
- container: image-instance
- runtime/engine: run the container instances

# Container vs. Virtual Machine
![[Pasted image 20231012090949.png]]
![[Pasted image 20231012091241.png]]
