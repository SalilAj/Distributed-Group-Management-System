# Distributed Group Management System

In distributed computing terminology, a ‘process group’ or ‘group’ is simply a set of cooperating processes distributed over one or more interconnected computers. 

## Requirements:
A ‘group membership management service’ should provide its members the following services: 
1.	Forming, joining, and leaving groups 
2.	Monitoring group members and reporting member failures to the remaining members 
    -	A failed process is deemed to have left a group
3.	Returning the current group membership when required
4.	Possibly providing a ranking of members 
    -	E.g., based on age 

It is usually the case that a failed process, or one that becomes disconnected from the other members of its group(s), is deemed to have left the group(s). 

The project is simply to design, implement and demonstrate a group membership management service that provides the (remaining) members of a group with a consistent view of its membership at any time and that tolerates the full range of failures that commonly arise in distributed systems, e.g., node or process failure, loss messages, and/or network partitions etc, etc. 

Note that it may be difficult to ensure that all nodes have the same view of the membership of a group at a particular point in time. Therefore, as a minimum, it is required that all members ‘see’ the same sequence of membership changes over time. Specifically, a list of the current members of a group is called the ‘group view’. Each group view will differ from the previous group view by the addition or deletion of exactly one member and the same sequence of group views should be available to each process over time. Hence, when a process sends a message, it is sent in the context of the sender’s current group view and the receiver can assess whether the view has changed on reception and act accordingly.

## Project:
Refer Report.pdf


