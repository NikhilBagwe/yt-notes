## Active Directory :

- AD lets Enterprise companies organize all their resources very easily at one place.
- The resources could be Servers, Employees, Files, Printers, etc.
- AD holds information about resources on the network.
- So we can say that AD is a hierarchial DB which stores data in a tree-like structure where we have parent-child relationship between Root domain -> Sub domain -> OUs -> Objects.
- Everything in an AD is closely related to Domain Name Server.

## AD Logical Architecture :

![3](https://github.com/NikhilBagwe/yt-notes/assets/67143015/3beeda5f-4bbf-4d09-b2b0-bc54b68b915c)


- Consider above example where duco.com is present in 3 diff. locations of world - us, europe and asia.
- Object - An Employee called as Object is the most basic entity of AD.
- OU - Objects can further be grouped/organised into Organizational Units (OU). OUs are general purpose containers available to admins in AD.
- Suppose 100 new employees are grouped into OU1. Now when admin wants to give access to a certain training folder to them, he can provide the access at OU1 level so all 100 employees can access it.
- Domain - An Active Directory domain (AD domain) is a collection of objects within a Microsoft Active Directory network.
- Tree - An Active Directory (AD) tree is a collection of domains within a Microsoft Active Directory network.  A tree is a combination of those objects and domains which share the same namespace.
- Forest - The group of many AD trees is called Forest. An Active Directory forest is the highest level of organization within Active Directory. Suppose if a company buys a new company. In this case we connect the Trees of both companies and form a Forest.

---

## LDAP : 

- Lightweight Directory Access Protocol.
- With help of LDAP we can access Directory services.
- Cross platform
- AD is a "Directory Service DB" and LDAP is a protocol used to talk with AD.

## Working of LDAP :

- When user enters it's ID and password in a system/app, LDAP makes a call to Server and checks if the User is valid or not.

## Why use LDAP ?

- Suppose you are working in a company of 10000 employees and you want to apply diff. policies to each groups(basically departments of company like HR, Accounts,etc) consisting of users.
- This task cannot be performed manually.
- Thus, with the help of LDAP we can create groups and attach policy to them easily.











