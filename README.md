# Kubernate with A REFERENCE
Its a part of the CI/CD pipeline
Availability

While in beta, GitHub CLI is available for repos hosted on GitHub.com only. It does not currently support repositories hosted on GitHub Enterprise Server or other hosting providers. We are planning support for GitHub Enterprise Server after GitHub CLI is out of beta (likely toward the end of 2020), and we want to ensure that the API endpoints we use are more widely available for GHES versions that most GitHub customers are on.

#Get The Availabality
#Kubernetes Cluster using Ansible

    Clone repository.
    Create multiple centos8 servers. One master and many worker. Use vagrant like here
    Change the “ad_addr” in the env_variables file with the IP address of the Kubernetes master node.
    Add the IP Addresses of the worker nodes and the master node in the “hosts” file.
    Run the following command to setup the Kubernetes Master node.

ansible-playbook setup_master_node.yml

    Once the master node is ready, run the following command to set up the worker nodes.

ansible-playbook setup_worker_nodes.yml

    Once the workers have joined the cluster, run the following command to check the status of the worker nodes.

kubectl get nodes
