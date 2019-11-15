---
layout: post
title: Team3 Domain Model decision
author: Team 3
categories: team3
---
In der ersten Version des [Domain Models](https://github.com/Archi-Lab-FAE/fae-team-3-documentation/wiki/Domain-Model) haben wir uns dazu entschieden keine Entitäten zu modellieren, die wir nicht selber verwalten müssen. Dementsprechend sind keine Entitäten für die dementiell veränderten Personen und deren Ansprechpartner modelliert.

Desweiteren gehen wir nach dem aktuellen Stand davon aus, dass wir eine Message oder einen API Call bekommen, der das Nachrichtensystem triggert. Da wir aktuell aber noch nicht genau sagen können, wie dieses Element aufgebaut ist, haben wir auch dieses bisher nur über die Attribute des Notfalls (Eingang und Typ) modelliert.

#### Anmerkungen SB 15.11. (bitte nach Bearbeitung löschen)
* das sind 2 Entscheidungen in einem File => besser trennen. Die zweite hat einen anderen Typ (open)
* die erste wird kaum durchzuhalten sein. Eine Begründung fehlt mir auch. 