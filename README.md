# k8s-workload-optimizer

## Overview
The main purpose of this project is to further optimize k8s workloads. Currently what happens is that *scheduler* assigns the workload to the any nodes having suffice resources. The pros and cons of this method are :- 

### Pros:- 
You can leave all headache to *scheduler*. It will take care of all the workload and assigns the pods to the nodes and guess what it comes out of box. 

### Cons :- 
Scheduler are not aware of underlying hardware and its cost. So sometimes it may assign pods where the cost of hardware is more so increasing the cost of complete infrastructure. In worse case there would be fragmentation in cluster. 

## Goals
Goal of this project is to reduce the cost of whole infrastructure by making *Kubernetes scheduler* aware of underneath hardware so that it can assign pod more efficiently. This will make *Kubernetes* more cloud dependent. Currently we are only supporting AWS as of now. 


## Proposed Solution 
We are using the power of *Pod's affinity* and *Mutating Webhooks* to achieve our solution. More and detailed part can be found on [solutions](docs/solution.md) page.


Deep and detail architecture can be found [here](docs/architecture.md)


