In Edge computing, there are scenarios where customers would like to have an whole cluster installed at edge location. As a result, 
admins/users can leverage the local control plane to implement management functionalities and take advantages of all edge computing's benefits.

For these use cases, when considering large set of edge locations, the resource usage of management plane adding together will be high. 
K3s is an opensource project enabling lightweight kubernetes cluster including the light control plane and worker components. 
KubeEdge is the other opensource project enabling lightweight k8s client on the edge nodes. The KubeEdge agent runtime memory footprint is 
10MB and it supports kubernetes types. Meanwhile KubEdge is targeted for Edge/IOT computing with many functionality enablements. 

By integrating KubeEdge and K3s, this proposal is to allow customers to run an efficient kubernetes cluster for Edge/IOT computing. 

# Architecture Design

# Protocol 

K8s client library interface will be used. The edgecontroller on each edge node only watches against k8s types for the node itself. 

# Work Items

1. Port current EdgeController code to KubeEdge agent side
2. Remove cloudhub/edgehub 
3. Come up with lightweight etcd
4. Lightweight kubeproxy on edgecore
5. E2E 


