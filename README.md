# ProductionChart

#### Features

* `ProductionChart` Dieses Control kann als _**CustomControl**_ verwendet werden.
* `TextfieldProduction` Dieses Control kann (anstelle von TextField) als _**BusinessControl**_ verwendet werden.
* `Liniendiagramm` Darstellung der Produktionen 2015 - 2018 in einem Liniendiagramm.
* `Dynamische Skalierung` Anhand der vier Werte wird realtime und dynamisch eine passende Skalierung festgelegt.
* `Grün/Rot Indikator` Je nachdem ob die Produktion gestiegen oder gesunken ist, wird die Linie Grün bzw. Rot eingefärbt.
* `Drag&Drop` Die Werte können mittels Drag&Drop eingestellt werden.
* `Direkte Eingabe` Die Werte können auch angepasst werden, indem der Wert angeklickt und geändert wird.
* `Validierung` Die Eingabe vom Benutzer wird validiert (nur Zahlen sind erlaubt).
* `Keyboard Eingabe` Befindet man sich im Textfeld, kann mittels Rauf- und Runter-Tasten der Wert um +-1 angepasst werden.
* `Shift+Ctrl+Alt` Hält man _Shift_ gedrückt werden 10er, mit _Shit+Ctrl_ 100er und mit _Shift+Ctrl+Alt_ 1000er Schritte gemacht.
* `Ansicht wechseln` Mit einem Klick auf das Icon oben rechts, wird die Ansicht zwischen _Kreisen_ und _Windrädern_ gewechselt.

## HowTo: Integration CustomControl `ProductionChart`
* `Daten kopieren` Ordner _productionChart_ an gewünschten Ort im Zielprojekt kopieren. (Inhalt von _ProductionChart.zip_)
* `Imports anpassen` Am einfachsten via Search&Replace. "to.be.defined" ersetzen durch Pfad im Zielprojekt. (Z.B. cuie.githubname.windpark)
* `private ProductionChart cc;` Variable erstellen 
* `cc = new ProductionChart();` Variable initialisieren
* `getChildren().add(cc);` ProductionChart einer View hinzufügen
* `cc.bind(pm.p15Property(), pm.p16Property(), pm.p17Property(), pm.p18Property());` Binding der Werte anhand der Hilfsfunktion bind()

## HowTo: Integration BusinessControl `TextfieldProduction`
* `Daten kopieren` Ordner _productionChart_ an gewünschten Ort im Zielprojekt kopieren. (Inhalt von _ProductionChart.zip_)
* `Imports anpassen` Am einfachsten via Search&Replace. "to.be.defined" ersetzen durch Pfad im Zielprojekt. (Z.B. cuie.githubname.windpark)
* `private p15, p16, p17, p18;` Variablen erstellen 
* `p15 = new TextfieldProduction(); p16 = new TextfieldProduction(); p17 = new TextfieldProduction(); p18 = new TextfieldProduction();` Variablen initialisieren
* `getChildren().addAll(p15, p16, p17, p18);` TextfieldProduction's einer View hinzufügen
* `bc.bind(p15, p16, p17, p18, pm.p15Property(), pm.p16Property(), pm.p17Property(), pm.p18Property());` Binding der Werte anhand der Hilfsfunktion bind()