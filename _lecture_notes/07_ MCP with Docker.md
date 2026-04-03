## 07_ MCP with Docker

### What is Docker?
- Containerization platform for packaging applications with their dependencies
- Lightweight virtualization using OS-level isolation
- "Build one, run anywhere" philosophy

### Docker Images
- Read-only templates containing application code, runtime, libraries, and dependencies
- Built-in layers using Dockerfile instructions
- Immutable snapshots that serve as blueprints for containers

### Docker Image Layers
- Layers are how Docker Images are built
  - Images are composed of read-only layers stacked on top of each other
  - Each Dockerfile instruction creates a new layer
  - Layers are cached and reusable across different images

### Docker Containers
- Running instances of Docker images
- Isolated processes with their own filesystems, network, and process space
- Stateful and ephemeral - can be started, stopped, moved and deleted

### Docker Registry
- Centralized storage and distribution system for Docker images
- Docker Hub as a default public registry
- Private registries for internal use (AWS ECR, Azure ACR, etc)
- Push/pull workflow: docker push and docker pull
- The official Docker Registry: Docker Hub
- AWS Docker Registry: ECR (Amazon Elastic Container Registry)
- Github Packages

### Docker Networking
- Default Bridge Network
  - Docker creates a virtual bridge (docker0) on the host
  - Each container gets its own virtual network interface
  - Containers can communicate with each other via internal IPs
  - NAT (Network Address Translation) handles external connectivity