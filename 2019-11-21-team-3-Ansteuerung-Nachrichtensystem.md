---
layout: post
title: Team3 Ansteuerung des Nachrichtensystems
author: Team 3
categories: global
---

Da das Erzeugen einer Ausnahmesituation eine kritische Aufgabe ist, sollte dieser Aufruf, egal um was für eine
Ausnahmesituation es sich handelt, synchron erfolgen. Da das Nachrichtensystem nicht für die Inhalte der übermittelten 
Daten verantwortlich ist und die zu versendenden Nachrichten auch nicht beschränkt werden sollen, nimmt das 
Nachrichtensystem die Nachrichteninhalte von anderen Systemen entgegen und erstellt diese nicht selber.

Des Weiteren benötigt das Nachrichtensystem in einer Ausnahmesituation die Tracker ID, damit es die Kontaktpersonen
ermitteln kann. Außer der Tracker ID und dem Inhalt der Nachricht wird aktuell nichts weiteres benötigt.
