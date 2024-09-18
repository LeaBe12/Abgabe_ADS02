# Verkaufspreisvorhersage

Studienarbeit ADS02 - Machine Learning und Reporting

## Daten

* Dieser Datensatz umfasst Informationen über Verkäufe von Wohnimmobilien, Eigentumswohnungen, Gewerbeimmobilien, Mehrfamilienhäusern und unbebautem Land aus den Jahren 2002-2023
* Link zur Quelle: https://data.milwaukee.gov/dataset/property-sales-data

## Variablen

| Name          | Beschreibung                                                   | Typ    |
|---------------|----------------------------------------------------------------|--------|
| PropertyID    | Eindeutige ID zur Identifikation                               | int64  |
| PropType      | Art der Immobilie                                              | Object |
| taxkey        | Steuerkennzeichnung der Immobilie                              | Object |
| Address       | Adresse der Immobilie                                          | Object |
| CondoProject  | Gibt an, ob Immobilie Teil eines Eigentumswohnprojekts ist     | Object |
| District      | Bezirk der Immobilie                                           | Object |
| nbhd          | Nachbarschaftsnummer der Immobilie                             | Object |
| Style         | Architekturstil der Immobilie                                  | Object |
| Extwall       | Außenwandmaterial der Immobilie                                | Object |
| Stories       | Anzahl der Immobilien-Stockwerke                               | float64|
| Year_Built    | Baujahr der Immobilie                                          | int64  |
| Rooms         | Anzahl der Zimmer in der Immobilie                             | Object |
| FinishedSqft  | Quadratmeterzahl des fertiggestellten Wohnraums                | int64  |
| Units         | Anzahl der Einheiten wie z. B. Wohnungen                       | Object |
| Bdrms         | Anzahl der Schlafzimmer                                        | Object |
| Fbath         | Anzahl der voll ausgestatteten Badezimmer                      | Object |
| Hbath         | Anzahl der halb ausgestatteten Badezimmer                      | Object |
| Lotsize       | Größe des zur Immobilie gehörenden Grundstücks                 | int64  |
| Sale_date     | Verkaufsdatum der Immobilie                                    |datetime|
| Sale_price    | Verkaufspreis der Immobilie                                    | int64  |


## Schritte zum Nachvollziehen und umsetzen
1) Die einzelnen Dateien der Jahre wurden zusammengefügt (Concat.ipynb)
2) Die EDA wurde durchgeführt, für tiefere Einblicke in die Daten (EDA.ipynb)
3) Die, für die Modelle verwendeten, Daten wurden in der EDA bearbeitet und als Parquet gespeichert (cleaned_data.parquet)
4) Verschiedene ML-Modelle wurden getestet und optimiert (Models.ipynb)
5) Das beste Modell wurde als Pickle-Datei gespeichert, um diese für die konkrete Vorhersage zu verwenden (Bestmodel.pkl)
6) Die pkl-Datei wird für die Vorhersage des Verkaufpreises verwendet (Vorhersage.ipynb)
