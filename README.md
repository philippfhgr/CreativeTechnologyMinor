# Creative Technology Minor

#### Interaktive Grafikerstellung durch Fingertracking in Touchdesigner
![WhatsApp Video 2025-06-23 um 15 11 54_e1d91f7f](https://github.com/user-attachments/assets/05de18ba-f556-4888-ac63-555e3ab73c3a)

## Schritt für Schritt Anleitung
### Ideenfindung

Was möchte ich erreichen? Wie sollte mein Endprodukt aussehen? Dafür ist es hilfreich, die Möglichkeiten durch andere Projekte auszuloten.
Das Endprodukt bestimmt auch die Art des In- und Outputs.

### Tracking

Touchdesigner aufsetzen: In Touchdesigner wird von links nach rechts gearbeitet. Für den Input der Kamera über MediaPipe das gewünschte Tracking einrichten. Hier können verschiedene Gesten gewählt werden. Ich habe den Index Finger 1 zum Malen und die Victory Gesture zum Reseten gewählt. Die Gesten sollten für die Kamera klar unterscheidbar sein.
https://github.com/google-ai-edge/mediapipe

Einen Kreis zum Malen per Circle TOS und einen um das Aussetzen des Trackings beim “Absetzen” durch den erhöhten Z-Index einfügen. Letzterer muss dann per Over auf das Endergebnis gelegt werden.

![Code](https://github.com/user-attachments/assets/fcd4ea7b-b94c-4996-b31d-259cf9fcbdef)

### Grafik

Über einen hochzählenden Timer vier Grafiken über einen Switch durchwechseln lassen. Darauf achten, dass die Grafiken über Zeit cross disolven. Nur mit dem Counter springen die Grafiken von einer zur nächsten. Die erste Grafik muss als fünfte Grafik nochmals eingefügt werden, da diese ansonsten nur die halbe Zeit gezeigt wird.

Danach den zuvor erstellten Circle als Maske per Composite über die Grafik legen. Diesen Circle ausschnitt, dann nach Belieben im Feedback anpassen. Ich habe Blur, Noise und Displace hinzugefügt. Die Noise lässt sich auch über die Zeit verändern. So bewegt sich die Grafik nach dem Zeichnen noch weiter und die Farben verfliesen immer mehr.

Dann fehlt nur noch der Output und das Project muss über Perform geöffnet werden.


## Komponentenplan
![KomponentenplanCT](https://github.com/user-attachments/assets/68ae3197-ee0d-4fad-b78d-42488fbc029e)


## Entwicklungsprozess
Der Entwicklungsprozess verlief flüssig und dem Präsenzunterricht nach. Zuerst haben wir gelernt, was Touchdesigner ist, dann den Output, danach die Grafiken und zum Schluss noch den Input mit MediaPipe. Zwischendurch haben wir unsere Vorstellung vom Endprodukt immer wieder angepasst und verändert, bis wir zum jetzigen Ergebnis gekommen sind.

## Verworfene Lösungsansätze
Zuerst hatten wir die Idee, dass mit den Händen an der Leinwand Inhalte gesteuert werden können. Möglich wäre zum Beispiel ein Wasserfall gewesen, bei dem das Wasser mit der Hand abgelenkt werden hätte können. Dafür hätten wir einen geeigneten Sensor (Lidar) gebraucht.
Eine andere Möglichkeit wäre das Zeichnen an der Wand mit der Hand gewesen. Dem sind wir mit dem Projekt schon recht nahe gekommen. Das hätte zum Sensor noch einen Kurzdistanz-Beamer oder einen Rückprojektor gebraucht. Mit einem regulären Beamer ist das ganze aber schon etwas einfacher.

## Fehlschläge und Umplanung
Wir wollten ursprünglich das Video im Iglu drehen. Aufgrund von Krankheit fiel der Plan aber ins Wasser. Ich hatte dann aber die Möglichkeit, an einem ebenfalls interessanten Ort zu drehen und ich denke, das Video ist trotzdem gut gelungen.

## Video
[![CTVideoF](https://github.com/user-attachments/assets/90d3fd08-563f-4520-8c8a-e2619b14cdab)](https://youtu.be/-pFldMDn9vs)

## Herausforderungen
Herausfordernd war zuerst ein Verständnis für die Kommunikation zwischen der digitalen und der analogen Welt zu entwickeln. Dort hat IM4 Physical Computing natürlich auch viel geholfen. Danach die ganze Übersetzung und was mit den Werten überhaupt alles angestellt werden kann. Ich musste mich zuerst in das neue Programm einfinden.

## Lerneffekt
Am Ende dieses Projektes kann ich sagen, dass ich mich in einem weiteren Programm auskenne. Einige besuchte Kunstausstellungen könnte ich jetzt auch nachstellen oder sogar noch verbessern durch den Zusatz der Interaktivität.
Natürlich hat Touchdesigner in Kombination mit MadMapper noch unzählige weitere Funktionen. Ich denke aber, dass ich für ein weiteres Projekt relativ schnell erste Ergebnisse liefern könnte.

## Aufgabenteilung
<li> Ideenfindung: Thomas & Philipp
<li> Touchdesigner: Philipp
<li> Interaktive Grafik: Philipp
<li> Dokumentation inkl. Grafiken: Philipp
<li> Videoproduktion und Postproduktion: Philipp (Darstellerin: Anina Branger)

## Known Bugs
Durch die Qualität der Webcam ist das Tracking nah an der Kamera am besten. Für weitere Distanzen bräuchte es eine höhere Qualität. Bei weiteren Distanzen funktioniert die Tiefenerkennung nicht zuverlässig bzw sind die Distanzunterschiede zwischen links oder rechts höher als die Usenden nach hinten zeigen können. Ein Absetzen des “Stiftes” ist somit kaum möglich, ausser die Usenden laufen weiter nach hinten, was aber nicht immer praktikabel ist.
Ausserdem ist die Handposition durch das Tracking mit MediaPipe etwas limitiert. Der Finger muss von vorne immer klar ersichtlich sein, ansonsten bricht das Tracking ab. Gerade bei runden Zeichenbewegungen ist das nicht optimal. Wenn die Usenden darauf achten, funktioniert es aber recht zuverlässig.
Ein weiterer Bug ist, dass immer der zuerst erkannte Finger getrackt wird. So kann es erscheinen, als würde das Tracking nicht funktionieren, dabei wird einfach der andere Finger erkannt.

## Planung
Ich habe mich für die Planung am Präsenzunterricht und den Coachings orientiert. So konnte ich sichergehen, dass ich immer in der Zeit lag und konnte Feedbacks einholen.

## Hilfsmittel
Da Touchdesigner ein grösstenteils visuelles Programm und zusätzlich nicht so verbreitet ist, war relativ schnell klar, dass es kein Steckenpferd von ChatGPT ist.
Die Community dahinter ist aber recht aktiv, weshalb ich auf viele Tutorials zurückgreifen konnte. Man sollte nur darauf achten, nicht genau das Gleiche nachzubauen, sondern seinen eigenen Twist einzubinden. Die grösste Ressource wird wohl Torin Blankensmith sein. Er ist auf verschiedenen Plattformen unterwegs und beschäftigt sich viel mit dem Thema Tracking.
