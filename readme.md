Run Kubernetes with Containerd instead of Docker using Ansible on Ubuntu

## Steps
1. Create the master and worker servers and ensure ssh login is working as root
2. Modify hosts to match the IP for master and nodes
3. Run: `$ ansible-playbook -i hosts 00_kube_deps.yaml`
4. Run: `$ ansible-playbook -i hosts 01_master.yaml`
5. Run: `$ ansible-playbook -i hosts 02_workers.yaml`
6. Log in to master server as `ubuntu` user and run: `kubectl get nodes`
7. Sudo to become root and run: `crictl pods`
