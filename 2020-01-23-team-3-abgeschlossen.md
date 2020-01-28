---
layout: post
title: Ausnahmesituation abschließen
author: team3
categories: team3
---

Dass das Abschließen von Ausnahmesituationen, wie in den [Szenarien](https://archi-lab.io/display/public/03+-+Integration+Scenarios+For+Case+Study) dargestellt, gewünscht ist, wurde vor dem Vortrag am 24.01.2020 bestätigt. 

Das genaue Vorgehen und die Fehlerbehandlung muss noch geklärt werden. Möglichkeiten das nicht getätigte Abschließen einer Ausnahmesituation zu behandeln wären beispielsweise:

- Nach einem Zeitraum X wird der Kontaktperson, die die Nachricht angenommen hat, eine weitere Nachricht mit der Frage, ob die Situation abgeschlossen ist, gesendet.
- Nach einem Zeitraum X wird die Nachricht an die nächste Kontaktperson weitergeleitet (Problem, wenn zwei Kontaktpersonen auftauchen)

Aufgrund der Szenarien wird aktuell nur die Möglichkeit geboten eine Ausnahmesituation abzuschließen. Aus Zeitgründen wurden keine der genannten Möglichkeiten bisher implementiert.

Um die Implementierung möglichst einfach zu halten und den Datenschutz zu vereinfachen, bedeutet das Abschließen einer Ausnahmesituation aktuell, dass diese aus dem System entfernt wird.
