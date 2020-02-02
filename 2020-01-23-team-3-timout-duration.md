---
layout: post
title: Timeout duration
author: team3
categories: team3
---

Wird eine [Nachricht](https://fae.archi-lab.io/glossary/2019/11/04/Glossary-Nachricht.html) an [Kontaktperson](https://fae.archi-lab.io/glossary/2019/11/06/Glossary-Kontaktperson.html) A versendet und es erfolgt innerhalb von `3` Minuten keine [Antwort](https://fae.archi-lab.io/glossary/2019/11/04/Glossary-Antwort.html), schickt das System automatisch eine Nachricht an Kontaktperson B mit der nächst höheren Priorität. 

Für den Fall, dass sich Kontaktperson A doch noch früher melden sollte als Kontaktperson B, bleibt die Antwort auf die Nachricht an Kontaktperson A noch offen und wird vom System nicht als abgelehnt gewertet. Diese Entscheidung wurde getroffen, da es im Falle einer [Ausnahmesituation](https://fae.archi-lab.io/glossary/2019/11/04/Glossary-Ausnahmesituation.html) am wichtigesten ist, der [Demenziell Erkrankten Person](https://fae.archi-lab.io/glossary/2019/11/15/Glossary-dementiell-Erkrankter.html) so schnell wie möglich zu helfen und es dabei keine Rolle spielt, welche Kontaktperson zur Hilfe eilt. Damit allerdings Kontaktperson A und B nicht gleichzeitig zur Hilfe eilen, wurde ein [Hilfe-Unterwegs-Mechanismus](https://fae.archi-lab.io/team3/2020/01/28/team-3-Hilfe-unterwegs.html) implementiert, der dies verhindern soll.

Der Zeitraum von `3` Minuten wurde gewählt, damit möglichst schnell eine Kontaktperson zur Hilfe eilt.

Für die Zeit der Entwicklung beträgt der Zeitraum allerdings 20 Sekunden, damit die Logik besser getestet und überprüft wreden kann.
