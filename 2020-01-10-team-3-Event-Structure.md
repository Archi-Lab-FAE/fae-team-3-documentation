---
layout: post
title: Event Structure
author: Team 3
categories: open
---

# Struktur von Events

Die Events, die wir mit Kafka versenden sollen der untenstehenden Struktur folgen.

Als Datentyp der gesendeten Events soll `json` verwendet werden.

Beispiel:

```json
{
    "id": "Generierte UUID des Events",
    "key": "UUID der betroffenen Entität",
    "version": "Fortlaufende Nummer für die Vergleichbarkeit der Aktualität des Events",
    "timestamp": "Unix-Timestamp",
    "type":"Der Typ des Events",
    "payload": {
        "id": "Die UUID der Entity",
        "field": "Ein Feld der Entity"
    }
}
```

Beispiel mit Datentypen:

```json
{
    "id": "5bc9f935-32f1-4d7b-a90c-ff0e6e34125a",
    "key": "0cfc04f1-6df5-42c6-a19a-146128b8a3b4",
    "version": 42,
    "timestamp": 1578665084,
    "type":"event-example-uploaded",
    "payload": {
        "payloadId": "0cfc04f1-6df5-42c6-a19a-146128b8a3b4",
        "field": "Das ist ein Feld und es enthält einen String"
    }
}
```