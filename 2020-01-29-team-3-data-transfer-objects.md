---
layout: post
title: Team3 Data-Transfer-Objects
author: Team 3
categories: team3
---

# Data-Transfer-Objects

Wir haben uns entschieden Data-Transfer-Objects (DTO) zu verwenden, um die Entites nicht komplett nach außen preiszugeben. Außerdem können einige der Annotationen in das DTO verschoben werden. Das bedeutet weiterhin, dass Änderungen an der Entity nicht zwangsläufig Änderungen am DTO benötigen. 

Das Verwenden von DTOs verringert einerseits die benötigte Anzahl von Methodenaufrufen und vereinfacht die Serialisierung der zu verschickenden Objekte.

Martin Fowler definiert DTOs wie folgt:
> An object that carries data between processes in order to reduce the number of method calls.

Als Grund für die Verwendung gibt er folgendes an:
> Although the main reason for using a Data Transfer Object is to batch up what would be multiple remote calls into a single call, it's worth mentioning that another advantage is to encapsulate the serialization mechanism for transferring data over the wire. By encapsulating the serialization like this, the DTOs keep this logic out of the rest of the code and also provide a clear point to change serialization should you wish.

[Martin Fowler on DTOs](https://martinfowler.com/eaaCatalog/dataTransferObject.html)