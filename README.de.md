<p align="center">
  <a href="README.md">Русский</a> | <a href="README.en.md">English</a> | <b>Deutsch</b>
</p>

# Entwurf eines Rundhohlleiters (6,21 GHz)

Dieses Repository enthält die analytischen Berechnungen und die Ergebnisse der dreidimensionalen elektromagnetischen Simulation eines Rundhohlleiters mit einem Anpassungsübergang, der für eine Betriebsfrequenz von **6,21 GHz** ausgelegt ist.

Das Projekt umfasst die Berechnung der geometrischen Parameter des Hohlleiterpfads, die Dimensionierung des Anpassungsglieds sowie die Überprüfung der Leistungsmerkmale der Struktur mittels Finite-Differenzen-Methode im Zeitbereich (FDTD).

---

## Projektstruktur

* `/calculations` — Mathematische Berechnungen der Hohlleiter- und Anpassungstransformator-Parameter im Mathcad-Format (`.xmcd`).
* `/simulation` — 3D-elektromagnetisches Simulationsprojekt in CST Studio Suite (`.cst`).
* `/docs/images` — Grafische Materialien und Screenshots der Ergebnisse.

---

## Analytische Berechnung

Die analytische Berechnung der geometrischen und elektrodynamischen Parameter (Hohlleiterradius, Grenzwellenlänge für den Grundmodus $H_{11}$, Wellenimpedanz) wurde in Mathcad durchgeführt. Die Basisabmessungen wurden unter Berücksichtigung von Frequenzbeschränkungen festgelegt, um einen Einmodenbetrieb zu gewährleisten.

### 1. Berechnung des Eingangshohlleiters (400 Ohm)
Bestimmung der geometrischen Grundmaße zur Gewährleistung der geforderten Wellenimpedanz auf der Betriebsfrequenz.
![Berechnung des Eingangshohlleiters](docs/images/calc_waveguide_400_ohm.png)

### 2. Berechnung des Anpassungsabschnitts
Berechnung der Parameter des Viertelwellentransformators zur Minimierung von Reflexionen an der Verbindungsstelle der beiden Abschnitte.
![Berechnung des Anpassungsglieds](docs/images/calc_matching_transformer.png)

### 3. Berechnung des Ausgangshohlleiters (800 Ohm)
Berechnung der Geometrie des Hohlleiters mit erhöhter Wellenimpedanz.
![Berechnung des Ausgangshohlleiters](docs/images/calc_waveguide_800_ohm.jpg)

---

## Numerische 3D-Simulation

Basierend auf den analytischen Berechnungen wurde in CST Studio Suite ein 3D-Modell eines Rundhohlleiters mit Bogen und Anpassungsübergang erstellt.

![3D-Modell des Hohlleiters](docs/images/simulation_3d_model.png)

### Ergebnisse der Z-Parameter-Analyse

Das Diagramm des Eingangsimpedanz-Betrags ($Z_{1,1}$) bestätigt die berechneten Parameter bei der Betriebsfrequenz:
* **Betriebsfrequenz:** 6,2106 GHz
* **Eingangsimpedanz ($Z_{1,1}$):** ~485 Ohm
* **VSWR (Stehwellenverhältnis):** ~1,2

![Diagramm der Z-Parameter](docs/images/simulation_z_parameters.png)

## Lizenz

Copyright (c) 2026 Ilya Kornilov

Dieses Quelldokument beschreibt Open-Source-Hardware (Open Hardware) und ist unter der Lizenz CERN-OHL-P v2 lizenziert.
Sie dürfen dieses Quelldokument unter den Bedingungen der CERN-OHL-P v2 (https://cern.ch/cern-ohl) verbreiten, modifizieren und darauf basierende Produkte herstellen.

Dieses Quelldokument wird OHNE JEGLICHE AUSDRÜCKLICHE ODER STILLSCHWEIGENDE GARANTIE verbreitet, EINSCHLIESSLICH DER GARANTIE DER MARKTGÄNGIGKEIT, DER ZUFRIEDENSTELLENDEN QUALITÄT ODER DER EIGNUNG FÜR EINEN BESTIMMTEN ZWECK. Bitte lesen Sie die Bedingungen der CERN-OHL-P v2 für weitere Details.
