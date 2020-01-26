---
layout: post
title: Service Layer
author: team3
categories: team3
---

Um die Controller möglichst kleinzuhalten, soll die gesamte Geschäftslogik in Service Klassen verschoben/erstellt werden, die in diesem Fall eine Service Layer bilden.

Hier beispielsweise der [`AusnahmesituationService`](https://github.com/Archi-Lab-FAE/fae-team-3-service/blob/master/src/main/java/de/th/koeln/archilab/fae/faeteam3service/ausnahmesituation/AusnahmesituationService.java), der Service-Methoden für Ausnahmesituationen bereitstellt:

```java
@Log
@Service
public class AusnahmesituationService {

    private AusnahmesituationRepository ausnahmesituationRepository;
    private NachrichtenService nachrichtenService;

    @Autowired
    public AusnahmesituationService(AusnahmesituationRepository ausnahmesituationRepository,
        TimeoutService timeoutService, NachrichtenService nachrichtenService) {
        this.ausnahmesituationRepository = ausnahmesituationRepository;
        this.nachrichtenService = nachrichtenService;
    }

    Ausnahmesituation saveAusnahmesituationAndSendMessage(Ausnahmesituation ausnahmesituation) {
        log.info("Ausnahmesituation wird gespeichert und Nachrichten versendet...");
        ausnahmesituation = ausnahmesituationRepository.saveAndFlush(ausnahmesituation);
        nachrichtenService.sendeNachrichtToKontaktperson(ausnahmesituation);
        return ausnahmesituation;
    }

    List<Ausnahmesituation> holeAlleAusnahmesituationen() {
        log.info("Ausnahmesituationen werden abgefragt...");
        return ausnahmesituationRepository.findAll();
    }

    Ausnahmesituation holeAusnahmesituation(String ausnahmesituationId) {
        log.info("Ausnahmesituationen mit ID " + ausnahmesituationId + " abgefragt...");
        return ausnahmesituationRepository.findById(ausnahmesituationId)
            .orElseThrow(AusnahmesituationNotFoundException::new);
    }

    void löscheAusnahmesiutation(String ausnahmesituationId) {
        log.info("Lösche Ausnahmesituationen mit ID: " + ausnahmesituationId);
        ausnahmesituationRepository.deleteById(ausnahmesituationId);
    }

    void löscheAlleAusnahmesituationen() {
        log.info("Löschen aller Ausnahmesituation wird durchgeführt...");
        ausnahmesituationRepository.deleteAll();
    }
}
```