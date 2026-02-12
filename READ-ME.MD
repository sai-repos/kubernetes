
1) First attach an IAM role with EKS/ADMIN permissions to the k8s Master server

2. Install EKSCLI

3. Install AWSCLI

      > aws configure ---login

4. Install KUBECTL

5. Login using --->> aws configure  or  --->> attach IAM role to the Master server

    now run eks.yaml file to create the cluster

    ## With yaml file

    > eksctl create cluster --config-file=eks-cluster.yaml

               [ or ]

    > eksctl create cluster -f eks-cluster.yaml

    ## Without yaml --waste

    > eksctl create cluster --name= "name"  --nodes= 3

6. Verify cluster creation:

    > eksctl get cluster

7. Configure kubectl to use your new cluster:

     > aws eks update-kubeconfig --name <name> --region <region>

8. Verify cluster connectivity:

     > kubectl get nodes

9. To delete the cluster

 > eksctl delete cluster -f eks-cluster.yaml

 without file 
  > eksctl delete cluster   --name sai-eks-cluster  --region ap-south-1

if u dont know the name of the cluster
  > eksctl get cluster
  
  done

or else u can delete nodes first
  >>> aws eks list-nodegroups --cluster-name sai-eks-cluster
 
 >>> aws eks delete-nodegroup \
  --cluster-name sai-eks-cluster \
  --nodegroup-name sai-managed-ng



