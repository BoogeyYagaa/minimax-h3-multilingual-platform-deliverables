---
title: "SaaS-Erklärvideos mit MiniMax H3: Was generiert werden sollte – und was nicht"
published: false
description: "Eine technische Trennung zwischen generierten Metaphern, echter SaaS-Oberfläche und der asynchronen MiniMax-H3-API."
tags: ai, webdev, api, tutorial
---

> **Offenlegung zur KI-Unterstützung:** Dieser Entwurf wurde mit KI-Unterstützung erstellt und am 14. August 2026 anhand der verlinkten MiniMax-Dokumentation geprüft. Die Beispiele wurden in dieser Arbeit nicht gegen ein reales Konto ausgeführt. Vor einer Veröffentlichung muss eine fachkundige Person Code, Parameter, Aussagezweck und Plattformkonformität selbst prüfen und verantworten. Der Beitrag enthält keine Affiliate- oder Tracking-Links.

Ein SaaS-Erklärvideo braucht zwei Bildsprachen. Generierte Szenen können ein abstraktes Problem zeigen: ungeordnete Daten, eine unterbrochene Übergabe oder einen Prozess, der sich sortiert. Sobald das Video jedoch erklärt, wo jemand klickt, welche Felder existieren oder welches Ergebnis die Software liefert, sollte die echte Oberfläche zu sehen sein.

Diese Trennung ist nicht nur redaktionell sinnvoll. Sie bestimmt auch, welche Dateien, Prompts und Prüfungen in einer technischen Pipeline benötigt werden.

![Abstrakte Datenbewegung vor einem leeren Monitor, in den später echte UI eingesetzt wird](./dev-minimax-h3-saas-explainer-1600x900.png)

## Die Grenze zwischen generierter Szene und Produktbeleg

| Aussage im Video | Geeignetes Material | Warum |
|---|---|---|
| „Der aktuelle Prozess ist unübersichtlich.“ | Generierte Metapher | Eine visuelle Verdichtung behauptet keine konkrete UI-Funktion. |
| „Daten aus mehreren Quellen kommen zusammen.“ | Metapher plus Sprechertext | Die genaue Integration muss separat belegt werden. |
| „Klicke hier, um einen Bericht zu erstellen.“ | Echtes Screen Recording | Klickpfad, Beschriftung und Zustand müssen zur aktuellen Version passen. |
| „Der Bericht enthält diese Felder.“ | Echtes Screen Recording | Generierte Felder wären nicht überprüfbar. |
| „Die Verarbeitung spart 30 Prozent Zeit.“ | Belegte Messung plus Quelle | Weder KI-Bild noch UI allein beweisen die Zahl. |
| „Das Produkt ist SOC 2-konform.“ | Aktuelle offizielle Compliance-Quelle | Security-Aussagen dürfen nicht aus einer Metapher abgeleitet werden. |

Eine einfache Regel reicht: **Metapher für Kontext, echte UI für überprüfbare Funktion.** Wenn eine Szene wie ein Produktbeleg aussieht, muss sie gegen das Produkt geprüft werden können.

## Was die offizielle MiniMax-H3-API dokumentiert

Die [offizielle Video-Generation-Anleitung](https://platform.minimax.io/docs/guides/video-generation) beschreibt MiniMax H3 als multimodales Videomodell für Text-, Bild-, Video- und Audioeingaben. Dokumentiert sind:

- Modellname `MiniMax-H3`;
- Auflösungen `768P` und `2K`;
- ganzzahlige Laufzeiten von 4 bis 15 Sekunden;
- Text-to-Video, First-/Last-Frame Image-to-Video und referenzbasierte Generierung;
- ein asynchroner Ablauf mit `task_id`, Statusabfrage und Download über `content.url`.

Die [V2-Referenz für das Erstellen einer Aufgabe](https://platform.minimax.io/docs/api-reference/video-generation-v2-create) verwendet `POST https://api.minimax.io/v2/video_generation`. Jede Anfrage braucht ein nicht leeres `text`-Element im `content`-Array.

Für reines Text-to-Video ist `ratio` verpflichtend und darf nicht `adaptive` sein. Bei First-/Last-Frame Image-to-Video bestimmt das Eingabebild das Verhältnis; ein anderes gültiges `ratio` wird als `adaptive` behandelt. Referenzgenerierung kann `adaptive` verwenden oder ein konkretes Verhältnis angeben.

Das sind dokumentierte Schnittstellenregeln. Sie sind noch kein Beleg dafür, dass der folgende Entwurf in einer bestimmten Konto-, Regions- oder Tarifkonfiguration erfolgreich läuft.

## Eine Text-to-Video-Aufgabe anlegen

Das kleinste nachvollziehbare Beispiel enthält nur die dokumentierten Pflichtfelder. Verwende keinen echten API-Schlüssel im Quelltext.

```bash
export MINIMAX_API_KEY="replace-with-a-local-secret"

curl --request POST \
  --url https://api.minimax.io/v2/video_generation \
  --header "Authorization: Bearer ${MINIMAX_API_KEY}" \
  --header "Content-Type: application/json" \
  --data '{
    "model": "MiniMax-H3",
    "content": [
      {
        "type": "text",
        "text": "In einem abstrakten Arbeitsraum fließen breite halbtransparente Bahnen aus fünf Richtungen auf eine freie Monitorfläche zu. Sie richten sich zu drei ruhigen parallelen Bahnen aus. Langsame Vorwärtsbewegung der Kamera, keine Zahlen, Logos oder lesbaren UI-Texte. Ende auf einer stabilen Komposition für ein später eingefügtes echtes Screen Recording."
      }
    ],
    "resolution": "2K",
    "duration": 8,
    "ratio": "16:9"
  }'
```

Bei Erfolg liefert der Create-Endpunkt eine `task_id`. Der Auftrag ist dann noch nicht fertig; Videoerzeugung ist asynchron.

### Warum der Prompt keine Oberfläche beschreibt

Der Prompt erzeugt absichtlich eine freie Monitorfläche. Die reale Produktaufnahme wird später eingesetzt. Dadurch kann das Team die filmische Einführung austauschen, ohne veraltete oder erfundene UI-Texte zu produzieren.

Auch Zahlen fehlen bewusst. Datenbahnen sind eine Metapher. Messwerte, Kundennamen und Compliance-Aussagen gehören in verifizierte Ebenen der Postproduktion.

## Status abfragen und Ergebnis speichern

Die offizielle Anleitung nennt für die Abfrage:

```text
GET https://api.minimax.io/v2/query/video_generation/{task_id}
```

Eine vorsichtige Python-Funktion kann Terminalzustände behandeln und nach Erfolg `task.content.url` zurückgeben:

```python
import os
import time
import requests

API_KEY = os.environ["MINIMAX_API_KEY"]
BASE_URL = "https://api.minimax.io"
HEADERS = {"Authorization": f"Bearer {API_KEY}"}


def wait_for_video(task_id: str, max_checks: int = 60) -> str:
    url = f"{BASE_URL}/v2/query/video_generation/{task_id}"

    for _ in range(max_checks):
        time.sleep(10)
        response = requests.get(url, headers=HEADERS, timeout=30)
        response.raise_for_status()

        task = response.json()["task"]
        status = task["status"]

        if status == "succeeded":
            return task["content"]["url"]

        if status in {"failed", "cancelled"}:
            raise RuntimeError(
                f"Video task ended with {status}: {task.get('error')}"
            )

    raise TimeoutError("Video task did not reach a terminal state")
```

`max_checks` ist eine Anwendungsgrenze, kein offizielles Service-Limit. Die dokumentierte Anleitung empfiehlt zehn Sekunden zwischen Abfragen. In einer Produktionsanwendung sollten zusätzlich Netzwerkfehler, temporäre URLs, Speicherung, Logging und Geheimnisverwaltung geprüft werden.

## Screen Recording und generierten Clip verbinden

Der technische Ablauf besteht aus zwei unabhängigen Quellen:

```text
generierter Kontextclip
  -> Qualitätsprüfung
  -> Schnittpunkt mit freier Fläche

echtes Screen Recording
  -> Versionsprüfung
  -> sensible Daten entfernen
  -> in die freie Fläche einsetzen

beide Quellen
  -> Sprechertext und Untertitel
  -> Fakten- und Markenprüfung
  -> Export
```

Das Screen Recording sollte aus derselben Produktversion stammen, die im Sprechertext genannt wird. Entferne Kundendaten, interne URLs, API-Schlüssel, E-Mail-Adressen und andere vertrauliche Informationen. Wenn das Produkt regelmäßig aktualisiert wird, speichere Aufnahmedatum und Versionsstand zusammen mit der Videodatei.

## Fehler nicht als kreative Abweichung behandeln

Die API-Referenz dokumentiert unter anderem Antworten für ungültige Parameter (`400`), fehlende Autorisierung (`401`), unzureichendes Guthaben (`402`), Inhaltsprüfung (`422`), Rate Limit (`429`) und Serverfehler (`500`). Anwendungen sollten diese Klassen unterscheiden.

- Ein fehlender Prompt wird durch erneutes Senden nicht besser.
- Ein `429` kann eine begrenzte Wiederholung rechtfertigen.
- Ein erfolgreicher Download kann trotzdem visuell unbrauchbar sein.
- Eine technisch gültige Metapher kann als Produktversprechen missverstanden werden.

Deshalb braucht die Pipeline zwei Gates: technische Dateiprüfung und redaktionelle Freigabe.

## Checkliste vor einer Veröffentlichung

- [ ] Eine fachkundige Person versteht und verantwortet alle Codebeispiele.
- [ ] Endpunkt, Felder, Statuswerte und Verhältnisregeln wurden erneut in der offiziellen Dokumentation geprüft.
- [ ] Code wurde in einer autorisierten Testumgebung ausgeführt oder ausdrücklich als ungetesteter Entwurf markiert.
- [ ] Es gibt keine Affiliate-, Referral-, Tracking- oder Vertriebslinks.
- [ ] Der Beitrag dient nicht primär dem Linkaufbau oder der Bewerbung eines Unternehmens.
- [ ] AI-Unterstützung ist am Anfang offengelegt.
- [ ] Generierte UI, erfundene Funktionen und unbelegte Kennzahlen wurden entfernt.
- [ ] Echte Aufnahmen enthalten keine sensiblen Daten.
- [ ] Die lokale und die entfernte DEV-Historie enthalten keinen zweiten, fast gleichen MiniMax-H3-Beitrag.

## Fazit

MiniMax H3 sollte im SaaS-Erklärvideo nicht die Benutzeroberfläche erfinden. Die API kann kurze Kontext- und Übergangsszenen erzeugen; der Produktbeleg kommt aus echten Screen Recordings und aktuellen Quellen. Technisch bedeutet das: dokumentierte V2-Anfrage, asynchrone Statusabfrage, getrennte Medienquellen und zwei Freigaben. Erst wenn eine fachkundige Person Code und Aussagezweck selbst geprüft hat, ist aus diesem Entwurf ein verantwortbarer DEV-Beitrag geworden.

---

## Quellen

- [MiniMax H3: Video Generation](https://platform.minimax.io/docs/guides/video-generation)
- [MiniMax H3: Create Video Generation Task](https://platform.minimax.io/docs/api-reference/video-generation-v2-create)

**SEO-Titel:** SaaS-Erklärvideos mit MiniMax H3: API, echte UI und Prüfgrenzen

**Beschreibung:** Technische Anleitung zur MiniMax-H3-V2-API und zur sauberen Trennung von generierten SaaS-Metaphern, echten Screen Recordings und überprüfbaren Aussagen.

**Tags:** `ai`, `webdev`, `api`, `tutorial`
