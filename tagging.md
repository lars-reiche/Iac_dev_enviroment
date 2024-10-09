# Tagging Konzept

Neben den Standard-Tags, die vom CCC automatisch für alle Resourcen und Infrastruktur-Objekte vergeben werden, sollen zusätzlich die folgenden Tags vergeben werden.  
Dies verbessert die Übersicht des Systems und erleichtert die Zuordnung und Abrechnung der Cloud-Kosten.  

## Tags für Inhaltsbeschreibung

Hiermit wird inhaltliche Zusammenfassung durchgeführt - beispielsweise alle Objekte der Wissensbasis.  

| Tag               | Bedeutung                                   | Beispiel                                                             | Default-Wert                    |
|:----------        |:------------                                |:----------                                                           |:----------------                |
| `Projekt`         | Projekt Name/id                             | `Wissensbasis`                                                       | `<leer>`                        |
| `Service`         | Anwendung / Service                         | `Wissensbasis`                                                       | `<leer>`                        |
| `Risiko`          | Risikobewertung nach AI-Act                 | `Wissensbasis`                                                       | `<leer>`                        |
| `Erstelungsdatum` | Datum der Erstellung/Veröffentlichung       | `Wissensbasis`                                                       | `<leer>`                        |



## Tags für organisatorische Zuordnung  

Hiermit werden Objekte, die nicht inhaltlich und strukturell durch das KI-CC verantwortet werden, ihren Besitzern zugeordnet.  

| Tag               | Bedeutung                                   | Beispiel                                                             | Default-Wert                    |
|:----------        |:------------                                |:----------                                                           |:----------------                |
| `Organisation`    | Einheit des EDEKA-Verbunds                  | `EZ` , `MH` (GHB Minden-Hannover), `SEH-xxx` (Einzehländler xxx)     | `E-IT`                          |
| `Leistungsschnitt`| Bereich / Abteilung / Geschäftsfeld         | `DACSS`, `EH1`,                                                      | `<DACSS>`                       |
| `Team`            | Team eines Bereichs                         | `Strategie`, `SRM`                                                   | `<KICC>`                        |

