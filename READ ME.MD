
1) First attach an IAM role with EKS/ADMIN permissions to the k8s Master server

2. install EKSCLI

3. Install AWSCLI

4. Install KUBECTL

5. now run eks.yaml file to create the cluster
    
    ## With yaml file
    > eksctl create cluster -f eks-cluster.yaml

    ## Without yaml --waste
    > eksctl create cluster --name= "name"  --nodes= 3

6. Verify cluster creation:

    > eksctl get cluster

7. Configure kubectl to use your new cluster:
    ## With yaml file
     > aws eks update-kubeconfig --name <name> --region <region>

8. Verify cluster connectivity:

     > kubectl get nodes

Now to delete the cluster
 
 > eksctl delete cluster -f eks-cluster.yaml