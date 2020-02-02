---
layout: post
title: Team3 Hilfe unterwegs
author: Team 3
categories: team3
---

Wenn eine [Kontaktperson](https://fae.archi-lab.io/glossary/2019/11/06/Glossary-Kontaktperson.html) zustimmt sich um die [Ausnahmesituation](https://fae.archi-lab.io/glossary/2019/11/04/Glossary-Ausnahmesituation.html) zu kümmern (`KANN_HELFEN`),
so werden alle weiteren [Antworten](https://fae.archi-lab.io/glossary/2019/11/04/Glossary-Antwort.html) von anderen Kontaktpersonen mit dem HTTP-Code 428 (`Precondition Required`) beantwortet 
und nicht persistiert.

Da durch den [Timer](https://fae.archi-lab.io/team3/2020/01/23/team-3-timout-duration.html) mehrere [Nachrichten](https://fae.archi-lab.io/glossary/2019/11/04/Glossary-Nachricht.html) im Umlauf sein könnten kann somit verhindert werden, dass mehrere Personen dem [demenziell Erkankten](https://fae.archi-lab.io/glossary/2019/11/15/Glossary-dementiell-Erkrankter.html) 
zur Hilfe eilen.

Bei zukünftiger Implementierung eines Frontends ist zu beachten, dass dieses Szenario gesondert behandelt wird.  
