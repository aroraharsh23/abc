# **Prerequisites**
A Kubernetes cluster that has been created and imported in Rancher GUI.
For detailed description of Racher installation and other documentation refer:

      https://rancher.com/


## **Choose the deployment**
### **Citrix Ingress Controller for VPX, MPX**
Download "citrix-k8s-ingress-controller.yaml" from the deployment Directory.

      wget  https://raw.githubusercontent.com/citrix/citrix-k8s-ingress-controller/master/deployment/baremetal/citrix-k8s-ingress-controller.yaml


Follow [deployment/baremetal](../baremetal) guide for description and to update the fields in the downloaded file.

Note: "nslogin" secret as described in the Deployment guide can also be created on "secret" section of Rancher GUI.

On Rancher GUI cluster page, click on "Launch Kubectl". It will open a terminal for Kubectl on the same page.
Create a new file in the launched terminal and copy paste the content of the updated yaml and use the following command.

      kubectl create -f <filename>

Launched application can be seen in the "workloads" sections of the cluster project on Rancher GUI.

### **CPX with builtin Controller**
Download "citrix-k8s-cpx-ingress.yml" from the deployment Directory.

      wget  https://raw.githubusercontent.com/citrix/citrix-k8s-ingress-controller/master/deployment/baremetal/citrix-k8s-cpx-ingress.yml

Follow [deployment/baremetal](../baremetal) guide for description.

Note: "nslogin" secret as described in the Deployment guide can also be created on "secret" section of Rancher GUI.

On Rancher GUI cluster page, click on "Launch Kubectl". It will open a terminal for Kubectl on the same page.
Create a new file in the launched terminal and copy paste the content of the yaml and use the following command.

      kubectl create -f <filename>

Launched application can be seen in the "workloads" sections of the cluster project on Rancher GUI.
