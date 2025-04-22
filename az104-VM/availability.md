## Availability set
1. An availability set is a logical feature you can use to ensure a group of related virtual machines are deployed together. 
2. The grouping helps to prevent a single point of failure from affecting all of your machines. 
3. The grouping ensures that not all of the machines are upgraded at the same time during a host operating system upgrade in the datacenter.

#### Upgrade domain
An update domain is a group of nodes that are upgraded together during the process of a service upgrade (or roll out).
**Azure only update one update domain at a time.**
#### Fault domain
A fault domain is a group of nodes that represent a physical unit of failure.

![0](/img/1-entraID/Capture4.PNG)