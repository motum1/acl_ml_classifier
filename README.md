# acl_ml_classifier

## paper_maestroni_motum_externe_validierung.ipynb

Dieses Notebook bündelt die zentralen Analyseschritte zur **internen und externen Validierung binärer Verletzungsmodelle** auf Basis von Excel-Datensätzen. Ziel ist es, Modellgüte, Generalisierbarkeit und Datenunterschiede zwischen internem und externem Datensatz systematisch zu prüfen.

Enthalten sind unter anderem:

- **Modellierungs- und Validierungspipelines** für verschiedene Algorithmen wie XGBoost, Logistic Regression, SVC und neuronale Netze
- **Interne Validierung** mittels wiederholter Cross-Validation
- **Externe Validierung** auf einem unabhängigen Datensatz
- **Kalibrationsanalysen** und **Decision-Curve-Analysen**, um die klinische Nutzbarkeit der Modelle besser einzuordnen
- **Post-hoc-Rekalibrierung** externer Vorhersagewahrscheinlichkeiten
- **Vergleich der Merkmalsverteilungen** zwischen internem und externem Datensatz zur Abschätzung eines möglichen Domain Shifts
- **Outlier-Erkennung** zur schnellen Datenqualitätskontrolle
- **Systematischer Modellvergleich** mehrerer Klassifikationsverfahren
- **Experimentelle Ansätze mit neuronalen Netzen und synthetischer Datenerweiterung**

Das Notebook dient damit als zentrale Arbeitsumgebung für die Frage, **wie stabil und übertragbar Verletzungsmodelle über verschiedene Datensätze hinweg sind** und wie sich Unterschiede in Datenstruktur und Kalibrierung auf die externe Modellleistung auswirken.
