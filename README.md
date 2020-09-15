# OpenShift Support Basics - Labs

These are labs that help to learn how to be functional for basic administration tasks.

## Getting Started

Connect to the EtherPad instance for the class to claim a username. Both links will be provided in the chat window of the class.

Sample URL: http://etherpad-labs.apps.cluster-cloudera-aa43.cloudera-aa43.example.opentlc.com/p/cloudera

Usernames have the format of user1 to user50 and the password is openshift.

## Architecture

### Accessing OpenShift

[Installing a web terminal](http://redhatgov.io/workshops/openshift_4_101/lab0-terminal/)

[Using the "oc" command line](http://redhatgov.io/workshops/openshift_4_101/lab1-welcome/)

### Finding pods and nodes

[Viewing Pods](https://docs.openshift.com/container-platform/4.5/nodes/pods/nodes-pods-viewing.html])

[Viewing Nodes](https://docs.openshift.com/container-platform/4.5/nodes/nodes/nodes-nodes-viewing.html)

## Network and Storage Labs

### Viewing Network Policies, Ingress, and Routes

[Network Policy](https://docs.openshift.com/container-platform/4.5/networking/network_policy/about-network-policy.html)

### Viewing StorageClasses, Persistent Volumes, and Claims

TBD

## Observability

[Accessing logs via CLI](https://docs.openshift.com/container-platform/4.5/logging/viewing/cluster-logging-viewing.html)

[Accessing logs via Web UI](https://docs.openshift.com/container-platform/4.5/logging/viewing/cluster-logging-visualizer.html)

[Examining cluster metrics in the Web UI](https://docs.openshift.com/container-platform/4.5/monitoring/cluster_monitoring/examining-cluster-metrics.html)

## Debugging

You can use [oc debug](https://docs.openshift.com/container-platform/4.5/cli_reference/openshift_cli/developer-cli-commands.html#debug) to open a shell to debug one of many OpenShift components.

```
$ oc debug node/ip-10-0-141-105.ec2.internal
Starting pod/ip-10-0-141-105ec2internal-debug ...
To use host binaries, run `chroot /host`

sh-4.2# cat /host/proc/cmdline
BOOT_IMAGE=/ostree/rhcos-... console=tty0 console=ttyS0,115200n8
rootflags=defaults,prjquota rw root=UUID=fd0... ostree=/ostree/boot.0/rhcos/16...
coreos.oem.id=qemu coreos.oem.id=ec2 ignition.platform.id=ec2 selinux=0

sh-4.2# exit
```

Using [oc exec](https://docs.openshift.com/container-platform/4.5/nodes/containers/nodes-containers-remote-commands.html) allows the remote execution of commands within the specified container within a pod.

```
$ oc exec mypod date
Thu Apr  9 02:21:53 UTC 2015
```

### Troubleshooting links

[Installation Troubleshooting](https://docs.openshift.com/container-platform/4.5/installing/installing-troubleshooting.html)

[Investigating pod issues](https://docs.openshift.com/container-platform/4.5/support/troubleshooting/investigating-pod-issues.html)

[Storage Issues](https://docs.openshift.com/container-platform/4.5/support/troubleshooting/troubleshooting-storage-issues.html)


# Other Resources

OpenShift Documentation - https://docs.openshift.com/

Kubernetes Documentation - https://kubernetes.io/docs/home/

Red Hat OPEN Training - https://connect.redhat.com/


OpenShift Learning Site - https://learn.openshift.com/

O'Reilly Katacoda - https://www.katacoda.com/courses/kubernetes

Complete Lab on Kubernetes - https://collabnix.github.io/kubelabs/

## CLI Guides

[oc](https://docs.openshift.com/container-platform/4.5/cli_reference/openshift_cli/getting-started-cli.html)

[odo](https://docs.openshift.com/container-platform/4.5/cli_reference/developer_cli_odo/understanding-odo.html)

[tkn](https://docs.openshift.com/container-platform/4.5/cli_reference/tkn_cli/op-tkn-reference.html)


[kubectl cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

[helm](https://helm.sh/docs/helm/)

[helm on OpenShift](https://docs.openshift.com/container-platform/4.5/cli_reference/helm_cli/getting-started-with-helm-on-openshift-container-platform.html)

## Extra debugging labs

https://www.katacoda.com/kierranm/scenarios/k8s-troubleshooting-01

https://www.katacoda.com/msv/scenarios/kubernetes-debugging

https://www.katacoda.com/andresguisado/courses/kubernetes101/debugging

https://www.katacoda.com/andresguisado/courses/kubernetes101/debugging-2

https://www.katacoda.com/contino/courses/kubernetes/debugging

