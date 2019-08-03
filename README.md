## Blog of psytester

Testing is my passion. Sharing knowledge is my contribution.

#### Smart Home == Smart Hack?

Naja wird ja wohl sicher sicher sein!!
...........Hmm, oder?

Ausgangslage: Eine Homematic CCU2 mit einer WebUI & SSH Access<br>

Zur Systemanalyse was alles installiert ist, in einer Console als root einloggen.
* welches Betriebssystem in welcher Version? ```cat/etc/os*```
* welche CPU Arch & Kernel Version? ```umame -a```
* Laufende Prozesse überprüfen auf weitere Software Anteile und welcher user genutzt wird: ```ps -afe```
* Welche Ports sind offen und welche Prozesse laufen darauf? ```netstat -tulpena```
* Welcher URL Aufruf geht über den lighttpd Webserver zu welchem Ziel Prozess? ```less /etc/lighttpd/conf.d/proxy.conf```

Vorbereitungen um das System anzusprechen:
* API Beschreibungen vom Hersteller suchen
* einschlägige Foren durchforsten
* Code Analyse mit Decompilern wie der Prozess funktioniert (Die undokumentierte System.Exec() Funktion ist in den Foren bekannt und auch die 'bessere' CUxD Ausweichfunktion)
* String Analyse einer Binary

Es kann losgehen....

Auflösung der Geschichte: Das Ergebnis war nicht gut: Smart Home == Smart Hack !<br>
Dieser Blog wurde geboren.
