Install RedHat OKD 3.11 on your own server.This install method is targeted for a single node cluster that has a long life.

This repository is a set of scripts that will allow you easily install the latest version (3.11) of OKD in a single node fashion.  What that means is that all of the services required for OKD to function (master, node, etcd, etc.) will all be installed on a single host.  The script supports a custom hostname which you can provide using the interactive mode.

**Please do use a clean CentOS system, the script installs all necesary tools and packages including Ansible, container runtime, etc.**

> **Warning about Let's Encrypt setup available on this project:**
> Let's Encrypt only works if the IP is using publicly accessible IP and custom certificates."
> This feature doesn't work with OpenShift CLI for now.

## Installation

1. Create a VM as explained in https://www.youtube.com/watch?v=ZkFIozGY0IA (this video) by Grant Shipley

2. Clone this repo

```
git clone https://github.com/vksinghibm/installcentos.git
```

3. Execute the installation script

```
cd installcentos
./install-openshift.sh
```
Finally you will this successful message
```
******
* Your console is https://console.169.62.247.131.nip.io:8443
* Your username is root 
* Your password is R75yzA2b 
*
* Login using:
*
$ oc login -u root -p R75yzA2b https://console.169.62.247.131.nip.io:8443/
******
Login successful.

You have access to the following projects and can switch between them with 'oc project <projectname>':

  * default
    kube-public
    kube-service-catalog
    kube-system
    management-infra
    openshift
    openshift-console
    openshift-infra
    openshift-logging
    openshift-monitoring
    openshift-node
    openshift-sdn
    openshift-template-service-broker
    openshift-web-console

Using project "default".
```


