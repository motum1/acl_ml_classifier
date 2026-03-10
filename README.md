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


## paper_neuronales_netz.ipynb

Dieses Notebook enthält experimentelle Analysen zur **synthetischen Datenerweiterung und Modellinterpretation** für neuronale Netze im Kontext der Verletzungsvorhersage. Der Fokus liegt darauf, Trainingsdaten kontrolliert zu augmentieren, deren Qualität zu prüfen und die Auswirkungen auf Modellleistung und Interpretierbarkeit zu untersuchen.

Enthalten sind unter anderem:

- **Framework zur synthetischen Datengenerierung** mit verschiedenen Verfahren, insbesondere Copula-basierter Augmentierung
- **Drift- und Qualitätsanalysen** zum Vergleich realer und synthetischer Daten anhand mehrerer statistischer Metriken und Visualisierungen
- **Quality-Assurance-Runner**, die synthetische Daten hinsichtlich Verteilung, Multivariatstruktur und Unterscheidbarkeit von realen Daten prüfen
- **Cross-Validation-basierte SHAP-Analysen**, um die wichtigsten Einflussfaktoren eines neuronalen Netzes zu identifizieren
- **Interne Modellpipeline** mit neuronalen Netzen, Copula-basierter Datenaugmentation, Kalibrationsanalyse und Decision-Curve-Analyse
- **Publikationsnahe SHAP-Visualisierungen**, die die wichtigsten Features und deren Einflussrichtung übersichtlich darstellen

Ziel des Notebooks ist es zu untersuchen, **wie synthetische Datenerweiterung die Modellstabilität, Interpretierbarkeit und Vorhersageleistung neuronaler Netze beeinflusst** und gleichzeitig sicherzustellen, dass die erzeugten Daten statistisch plausibel bleiben.


