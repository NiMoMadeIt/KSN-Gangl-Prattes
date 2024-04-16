# KSN-Gangl-Prattes
File Source: Hier wird das Eingangssignal geladen. In diesem Fall ist es ein RadioSignal.

LowPass Filter (mit Verkleinerung um Faktor 120): Das Signal wird durch einen Tiefpassfilter geleitet, der alle Frequenzen oberhalb von 40 kHz abschneidet und gleichzeitig die Datenrate reduziert.

Waterfall, Frequenzy Sink: Das Spektrum des Signals wird in Echtzeit angezeigt, damit du sehen kannst, welche Frequenzen im Signal enthalten sind.

Rational Resampler (mit Interpolation 1, Verkleinerung um Faktor 5): Die Abtastrate des Signals wird verändert, um es für die weitere Verarbeitung anzupassen.

FM-Demodulator (mit Audioverkleinerung um Faktor 8): Das FM-Radiosignal wird in ein Audiosignal umgewandelt, das wir hören können. Es wird auch dafür gesorgt, dass die Audiosignalfrequenzen im für uns hörbaren Bereich liegen.

Audio sink: Das demodulierte Audiosignal wird über Lautsprecher oder Kopfhörer ausgegeben, sodass du die Musik oder den Ton hören kannst.
