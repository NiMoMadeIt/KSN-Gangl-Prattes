# KSN-Gangl-Prattes
File Source: Hier wird das Eingangssignal geladen. In diesem Fall ist es ein RadioSignal.

LowPass Filter (mit Verkleinerung um Faktor 120): Das Signal wird durch einen Tiefpassfilter geleitet, der alle Frequenzen oberhalb von 40 kHz abschneidet und gleichzeitig die Datenrate reduziert.

Waterfall, Frequenzy Sink: Das Spektrum des Signals wird in Echtzeit angezeigt, damit du sehen kannst, welche Frequenzen im Signal enthalten sind.

Rational Resampler (mit Interpolation 1, Verkleinerung um Faktor 5): Die Abtastrate des Signals wird verändert, um es für die weitere Verarbeitung anzupassen.

FM-Demodulator (mit Audioverkleinerung um Faktor 8): Das FM-Radiosignal wird in ein Audiosignal umgewandelt, das wir hören können. Es wird auch dafür gesorgt, dass die Audiosignalfrequenzen im für uns hörbaren Bereich liegen.

Audio sink: Das demodulierte Audiosignal wird über Lautsprecher oder Kopfhörer ausgegeben, sodass du die Musik oder den Ton hören kannst.


#Zweites Radio

1.	Variablen hinzufügen:
   	Definition von `samplerate` und `frequency_shift` zur Steuerung der Abtastrate und Frequenzverschiebung des Signals.
2.	File Source Block:
   	Hinzufügen eines Blocks welches Radio Signale enthält.
3.	QT GUI Range Blocks:
   	Einrichten von Schiebereglern für RF-Verstärkung, Lautstärke und Frequenzverschiebung in der Benutzeroberfläche.
4.	QT GUI Sync Block:
   	Synchronisation der Benutzeroberfläche mit dem Flowgraph zur Visualisierung des Eingangssignals.
5.	Tiefpassfilter:
   	Hinzufügen eines Filters zur Entfernung unerwünschter Frequenzkomponenten im Eingangssignal.
6.	Rationale Resampling Block:
   	Anpassung der Abtastrate des Signals für weitere Verarbeitungsschritte.
7.	Komplex zu Float Block:
   	Umwandlung des komplexen Signals in ein reelles Signal.
8.	Hilbert Blocks:
   	Erzeugung des analytischen Signals für die FM-Demodulation.
9.	Subtraktionsblock:
   	Subtraktion zweier Signale zur Demodulation des FM-Signals und Extraktion des Audiosignals.
10.	Multiplikationsblock:
    Anpassung der Lautstärke des Audiosignals basierend auf Benutzereingaben.
11.	Audio Sink Block:
    Ausgabe des demodulierten Audiosignals über die Soundkarte des Computers.
 
