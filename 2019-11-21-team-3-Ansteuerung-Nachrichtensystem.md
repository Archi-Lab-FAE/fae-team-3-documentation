---
layout: post
title: Team3 Ansteuerung des Nachrichtensystems
author: Team 3
categories: global
---

Da das Erzeugen einer [Ausnahmesituation](https://fae.archi-lab.io/glossary/2019/11/04/Glossary-Ausnahmesituation.html) eine kritische Aufgabe ist, sollte dieser Aufruf, egal um was für eine
Ausnahmesituation es sich handelt, synchron erfolgen. Da das Nachrichtensystem nicht für die Inhalte der übermittelten 
Daten verantwortlich ist und die zu versendenden [Nachrichten](https://fae.archi-lab.io/glossary/2019/11/04/Glossary-Nachricht.html) auch nicht beschränkt werden sollen, nimmt das 
Nachrichtensystem die Nachrichteninhalte von anderen Systemen entgegen und erstellt diese nicht selber.

Des Weiteren benötigt das Nachrichtensystem in einer Ausnahmesituation die [Positionssender](https://fae.archi-lab.io/glossary/2019/11/15/Glossary-Positionssender.html) ID, damit es die [Kontaktpersonen](https://fae.archi-lab.io/glossary/2019/11/06/Glossary-Kontaktperson.html)
ermitteln kann. Außer der Positionssender ID und dem Inhalt der Nachricht wird aktuell nichts weiteres benötigt.
