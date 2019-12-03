---
layout: post
title: Swagger zur Dokumentation der API verwenden
author: Team 3
categories: guide
---

# Guide für die Verwendung von Swagger

Eine einfache Möglichkeit die eigenen Schnittstellen zu dokumentieren bietet [Swagger](https://swagger.io/).
Unter anderem erlaubt dies das Testen von Schnittstellen mit einem interaktiven Interface.

## Dependency

Zunächst einmal reicht es in der `pom.xml` folgende Dependency hinzuzufügen:

```xml
<dependency>
  <groupId>org.springdoc</groupId>
  <artifactId>springdoc-openapi-ui</artifactId>
  <version>1.1.49</version>
</dependency>
```

Diese analysiert die Controller und generiert daraus automatisch die Dokumentation.

## Konfiguration

```java
// Annotationen von Swagger
import io.swagger.v3.oas.annotations.Operation;
import io.swagger.v3.oas.annotations.tags.Tag;

// [...]

// Hinzufügen von Beschreibungen und Namen
@Tag(name = "BeispielEntity", description = "BeispielEntity API")
@RestController
public class BeispielEntityController {

    // Mit operation können Details erläutert werden
    @Operation(
        summary = "BeispielEntity erstellen",
        description = "",
        tags = { "BeispielEntity" }
    )
    @PostMapping(
        value = "/beispielentity/{beispielEntityId}",
        consumes = {"application/json"}
    )
    public BeispielEntity createBeispielEntity(/* [...] */) {
        // [...]
    }
}
```

Damit die interaktiven Beispiele auf der Dokumenationsseite funktionieren, 
muss in der `@PostMapping()` Annotation der Parameter `consumes` übergeben werden.

Weitere Informationen zu Swagger können der [offiziellen Dokumentation](https://swagger.io/docs/) entnommen werden.

## Postman

Bei der erstellung der Dokumentation erzeugt Swagger eine Datei namens
`openApi.json`. Diese kann zum Testen auch als Collection in Postman importiert werden.
