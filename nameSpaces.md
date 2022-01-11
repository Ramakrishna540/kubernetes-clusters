# Working with Kubernetes Namespaces
## Introduction
Namespaces are a central component of any Kubernetes infrastructure. This lab will give you the opportunity to work with namespaces in a functioning cluster. You will be able to practice the process of creating, using, and navigating Kubernetes namespaces.

## Solution
Log in to the provided control plane node server using the credentials provided:
```
ssh cloud_user@<PUBLIC_IP_ADDRESS>
```
### Create the dev Namespace
Create a namespace in the cluster called dev:
```
kubectl create namespace dev
```
### Get a List of the Current Namespaces
List the current namespaces:
```
kubectl get namespace
```
Save the namespaces list to a file:
```
kubectl get namespace > /home/cloud_user/namespaces.txt
```
Verify the list saved to the file:
```
cat namespaces.txt
```
We should see the list of namespaces.

### Find the quark Pod's Namespace
Locate the quark pod:
```
kubectl get pods --all-namespaces
```
Copy the name of the namespace where the quark pod is located.

Create a file in which to save its name: :
```
vi /home/cloud_user/quark-namespace.txt
```
Paste in the name of the quark pod's namespace.

Save and exit the file by pressing Escape followed by :wq.

## Conclusion
Congratulations on successfully completing this hands-on lab!

