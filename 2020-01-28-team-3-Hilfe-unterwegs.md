---
layout: post
title: Team3 Hilfe unterwegs
author: Team 3
categories: team3
---

Wenn eine Kontaktperson zustimmt sich um die Ausnahmesituation zu kümmern (`KANN_HELFEN`),
so werden alle weiteren Antworten von anderen Kontaktpersonen mit dem HTTP-Code 428 (`Precondition Required`) beantwortet 
und nicht persistiert.

Da durch den [Timer](https://github.com/Archi-Lab-FAE/fae-team-3-documentation/blob/master/2020-01-23-team-3-timout-duration.md) mehrere Nachrichten im Umlauf sein könnten kann somit verhindert werden, dass mehrere Personen dem demenziell Erkankten 
zur Hilfe eilen.

Bei zukünftiger Implementierung eines Frontends ist zu beachten, dass dieses Szenario gesondert behandelt wird.  
