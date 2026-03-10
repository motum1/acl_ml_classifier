# ACL_ML_Classifier

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


## paper_roc_auc.ipynb

Dieses Notebook fokussiert auf den **Vergleich mehrerer Klassifikationsmodelle** sowohl im internen als auch im externen Setting. Ziel ist es, die Modelle systematisch danach zu beurteilen, wie gut sie innerhalb des eigenen Datensatzes und auf einem unabhängigen externen Datensatz generalisieren.

Enthalten sind unter anderem:

- **Externe Validierung mehrerer Modelle**, trainiert auf dem Motum-Datensatz und getestet auf dem Maestroni-Datensatz
- **Vergleich zentraler Gütemaße** wie AUROC, LogLoss und Brier Score inklusive Bootstrap-Konfidenzintervallen
- **Gemeinsame ROC-Darstellungen**, um die externe Modellleistung direkt visuell zu vergleichen
- **Interner Modellvergleich** über wiederholte Cross-Validation mit OOF-Vorhersagen
- **Kombination aus threshold-freien und threshold-basierten Kennwerten**, um sowohl die generelle Trennschärfe als auch die praktische Klassifikationsleistung zu bewerten
- **Übersichtliche Ergebnistabellen**, die den Vergleich der Modelle kompakt zusammenfassen

Ziel des Notebooks ist ein klarer Überblick darüber, **welche Modelle intern robust performen und welche ihre Leistung auch auf externe Daten am besten übertragen können**.

## paper_shap_final.ipynb

Dieses Notebook fokussiert auf die **globale und lokale Interpretierbarkeit von Verletzungsmodellen** mithilfe von SHAP. Es untersucht, welche Merkmale die Modellvorhersagen über viele Cross-Validation-Durchläufe hinweg am stärksten beeinflussen, in welche Richtung diese Effekte wirken und wie stabil diese Muster über Personen hinweg sind.

Enthalten sind unter anderem:

- **SHAP-Analysen für logistische Regression und XGBoost** auf Basis wiederholter Cross-Validation
- **Globale Feature-Rankings**, um die wichtigsten Einflussgrößen der Modelle zu identifizieren
- **Vergleich von Effektstärke und Effektrichtung**, also nicht nur wie wichtig ein Merkmal ist, sondern auch ob es eher in Richtung „verletzt“ oder „unverletzt“ wirkt
- **Konsistenzprüfungen der SHAP-Erklärungen**, um sicherzustellen, dass die SHAP-Werte mit den Modellvorhersagen übereinstimmen
- **Übersichtliche globale SHAP-Visualisierungen**, sowohl für alle Merkmale als auch fokussiert auf die wichtigsten Top-Features
- **Subjektbezogene SHAP-Auswertungen** mit statistischen Kennzahlen und Konfidenzintervallen
- **Lokale SHAP-Waterfall-Plots**, um einzelne Vorhersagen anschaulich und nachvollziehbar zu erklären

Ziel des Notebooks ist es, die entwickelten Modelle nicht nur hinsichtlich ihrer Leistung, sondern auch hinsichtlich ihrer **inhaltlichen Nachvollziehbarkeit und Interpretierbarkeit** transparent darzustellen.
