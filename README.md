**1. Cluster Architecture, Installation, and Configuration (25%)**

This domain focuses on setting up and managing a Kubernetes cluster.

   ** Key Topics:**
        **Kubernetes Architecture:** Master and worker node components, control plane components (API Server, Scheduler, Controller Manager), etcd, and kubelet.
        **etcd Backup and Restore:** Set up etcd, perform backups, and restore etcd from snapshots.
        **Kubeadm Installation:** Set up clusters with kubeadm, troubleshoot initialization errors.
        **Networking:** Configure pod networking (e.g., Flannel, Calico), understand CNI plugins, DNS, and cluster IP networking.
        **Certificates:** Manage certificates using kubeadm, understand certificate authority (CA) and key pairs.
        **Security and Authentication:** Implement Role-Based Access Control (RBAC), configure Service Accounts, manage role bindings, and kubeconfig files.
        **Node Operations:** Join nodes to clusters, remove nodes, and configure taints/tolerations for node placement.

    **Preparation Steps:**
        Set up clusters on virtual environments using Minikube, Kind, or kubeadm on cloud VMs to get hands-on experience with different configurations.
        Practice etcd snapshots and restores and become familiar with etcdctl commands.
        Use kubeadm to create a cluster from scratch, focusing on managing certificates and troubleshooting network plugin setup.
        Apply RBAC policies on clusters to control access and test with different Service Accounts and role configurations.

**2. Workloads and Scheduling (15%)**

This section involves deploying applications and controlling their scheduling and behavior.

    Key Topics:
        **Pod Lifecycle:** Understand different Pod phases, restart policies, and readiness and liveness probes.
        Deployments, ReplicaSets, and DaemonSets: Create and manage workloads for replication and fault tolerance.
        Jobs and CronJobs: Configure batch jobs, schedule recurring jobs, and set up job cleanup policies.
        Manual Scheduling: Use node selectors, affinity/anti-affinity rules, and tolerations to influence pod placement.
        Scaling: Scale workloads up and down, using both manual scaling and Horizontal Pod Autoscaler (HPA).
        Rolling Updates and Rollbacks: Manage application updates, rollback deployments, and observe changes in workloads.

    Preparation Steps:
        Practice deploying Deployments, DaemonSets, Jobs, and CronJobs. Experiment with different configurations in YAML files.
        Simulate node failure scenarios and manually schedule Pods to specified nodes.
        Set up probes for readiness and liveness, and configure rolling updates/rollbacks on deployments.
        Configure HPA to auto-scale based on CPU/memory usage, and observe its behavior.

3. Services and Networking (20%)

This domain emphasizes network configurations and Services for communication in Kubernetes.

    Key Topics:
        Cluster Networking: Pod-to-pod communication, cluster IP routing, and troubleshooting network issues.
        Services: Configure ClusterIP, NodePort, and LoadBalancer services to expose applications.
        Ingress Controllers and Resources: Set up Ingress resources to expose HTTP and HTTPS routes, and manage ingress rules.
        Network Policies: Configure and enforce Network Policies to control access between pods.

    Preparation Steps:
        Deploy different types of Services (ClusterIP, NodePort, LoadBalancer) to expose applications, and troubleshoot connection issues.
        Practice configuring Ingress controllers and create ingress rules to handle HTTP(S) traffic. Experiment with different ingress annotations and TLS settings.
        Define and apply Network Policies to control communication between pods. Test policies to ensure they enforce desired restrictions.

4. Storage (10%)

The storage domain covers persistent data management in Kubernetes.

    Key Topics:
        PersistentVolumes (PV) and PersistentVolumeClaims (PVC): Configure PVs and PVCs for persistent storage in applications.
        StorageClasses: Manage dynamic provisioning, and understand storage class parameters and reclaim policies.
        Volume Management: Use volumes (emptyDir, hostPath, and configMap volumes) and set up volumes in pods.

    Preparation Steps:
        Create PVs and PVCs and test their binding process. Practice deploying applications that use persistent storage.
        Use StorageClasses to dynamically provision PVs. Experiment with different reclaim policies (Retain, Delete, and Recycle).
        Test volume mounts in pods and configure different types of volumes (e.g., emptyDir, hostPath) in different workloads.

5. Troubleshooting (30%)

Troubleshooting is critical and often the most challenging part of the exam.

    Key Topics:
        Application Failures: Debug issues with pods, containers, and application configurations.
        Control Plane Failures: Diagnose and resolve issues with the Kubernetes control plane components.
        Worker Node Failures: Handle worker node problems, such as unresponsive nodes and kubelet failures.
        Networking Failures: Diagnose and fix network-related issues, such as DNS problems, service connectivity issues, and network policies.
        Cluster Component Logs: Use kubectl logs, kubectl describe, and kubectl get events for insight into cluster health.

    Preparation Steps:
        Practice diagnosing issues with different components. For example, test scenarios where pods fail to start or services fail to route traffic.
        Familiarize yourself with common troubleshooting commands, such as kubectl logs, kubectl describe, and kubectl exec.
        Induce common failures by misconfiguring pods, services, or networking components, and then resolve them.
        Review control plane logs and node status when investigating cluster-level issues.
