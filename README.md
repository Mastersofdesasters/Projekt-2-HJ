# Projektseite-2-HJ

## [_Konzept_](#Konzept)
## [_Programm_](#Programm)
## [_Code_](#Code)

### Konzept <a name="Konzept"></a>
Für unser zweites Projekt wollten und sollten wir kein weiteres Spiel entwickeln, weswegen wir auf das generelle Prinzip eines (Zufalls)Generators gekommen sind. Das neue Projekt besteht aus mehreren verschiedenen Einzel-Programmen, welche sich aber alle dem Oberthema des Zufallsgenerators zuordnen lassen.
Das erste Programm ist ein Datums-Generator: Dabei gibt der Nutzer ein beliebiges Datum - auch ein Schaltjahr ist möglich - in das Programm ein und dieses gibt dann den zu dem Datum gehörenden Wochentag heraus. Außerdem zeigt das Programm ein Ereignis an, welches an diesem Tag passiert ist.
Das zweite Programm ist ein Zufallsgenerator für Zahlen, ähnlich dem "Kaffeelotto" von Siri: Dabei drückt der Nutzer auf den "Startbutton", und das Programm, ähnlich wie ein Glücksrad, generiert eine zufällige Zahl.

### Programm <a name="Programmm"></a>
Unsere Projekte haben wir im zweiten Halbjahr mit der Programmiersprache [PyCharm](https://www.jetbrains.com/pycharm/promo/?msclkid=cf1f147d283316267af377c347d0267c&utm_source=bing&utm_medium=cpc&utm_campaign=EMEA_en_DE_PyCharm_Branded&utm_term=pycharm&utm_content=pycharm) programmiert. Dies ist eine Entwicklungsumgebung (IDE Integrated Development Environment) der Sprache "Python" von dem Unternehmen "Jetbrains". Im Gegensatz zu "Python", das eher für erfahrenere Programmierer geeignet ist, ist PyCharm eine für Anfänger geeignete Umgebung. So sucht sie selbstständig - diese Funktion hat uns auch besonders beim Programmieren unserer Projekte geholfen - Fehler (z.B. Typos oder fehlende Klammern, Buchstaben etc.) und zeigt diese mit einer kleinen Glühlampe direkt in der betroffenen Zeile an. Klickt man dann auf die Glühlampe, so stellt PyCharm auch einen Vorschlag, wie dieses Problem behoben werden könnte, z.B. durch Umbenennung oder Ergänzung der fehlenden Zeichen. Auf der Suche nach einem passenden Programm hatten wir auch Java ausprobiert, jedoch kamen wir damit nicht so richtig zurecht. PyCharm gefiel uns dann auch aufgrund der farbigen Gestaltung, die es einfacher gestaltete, zu einzelnen Funktionen zu gelangen, am besten.
![Screenshot (34)](https://user-images.githubusercontent.com/111355300/221171875-94ad2a43-4244-4aaa-acfc-0f11cbaa430c.png)


### Code <a name="Code"></a>
*1.Programm*: 
Zuerst haben wir unseren Datums-Generator programmiert. Hierfür ist zunächst der Begriff ,,import" sehr wichtig. Mit diesem haben wir den ,,calendar" importiert, welcher in sogenannten Modulen/Packages auf PyCharm vorinstalliert ist. Hiermit hatten wir also unsere Grundlage für das Programm und PyCharm konnte auf alle Daten zugreifen. 
Als nächstes ist es wichtig dem Programm die zu errrechnende Variable zu geben bzw. diese zu definieren. In unserem Fall war das ,,findday(dates)", dies macht man mit dem Kurzbefehl ,,def", also bei uns ,,def findday(dates)". Wenn man nun die Enter-Taste drückt, springt man in die Zeile, wo man diese Variable richtig definiert. Wir mussten PyCharm nun also beibringen, wie er daten schreibt bzw. wenn sie vom User eingegeben werden, wie ee sie liest, also von Tag nach Jahr. Dafür haben wir ihm diese Begriffe gegegeben ,,day, month, year" und ihm dann gesagt woher er sie später bekommt bzw. wo er sie ablesen kann und zwar schreibt der Nutzer das Datum zwischen "..." , z.B. "06 04 2023". Dies haben wir mit "(int(i) for i in dates.split(" ")" programmiert, diesen Befehl findet man bei [PyCharm](https://www.jetbrains.com/pycharm/promo/?). 
Nun ging es an den Teil, PyCharm beizubringen, woher er das WIssen nimmt, welcher Tag das Datum war. Dazu haben wir die Variable ,,daynumber" eigeführt und diese definiert. PyCharm sollte das Datum mit Hilfe des ,,calendars" prüfen bzw. daher das Wissen nehmen, welcher Tag es war. Dazu haben wir ,,daynumber" mit "=" definiert, als ,,calendar.week(year,month, day). In umgekehrter Reihnfolge zu dem wie man ein Datum liest, da er im Kalender erstmal das richtige Jahr, dann den richhtigen Monat und dann den genauen Tag finden muss, denn es gibt ja z.B. viele 01.12, aber nur ein 2022. 
Ein weitrerer wichtiger Schritt war es die Wochentage zu definieren, weil das schlussendliche Ziel ja die Ausgabe des Wochentages zum Datum ist. Dafür haben wir die Variable ,,days" definiert und einfach die Wochentage aufgelistet. Wichtig hierbei war es sie immer in doppelten Strings zu schreiben, da wir im oben beigebracht hatten, dass das Datum in doppelten Strings eingegeben wird. Wir hatten nun also ,,days= [ "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]. 
Nun waren wir am Ende des Programms und wir haben ihm mit dem Befehl ,,return" beigebracht die beiden definierten Variablen "daynumber" und "days" zu verbinden, sodass er das im Kalender gefundene Datum als Wochentag wiedergibt.
Zum Schluss haben wir die Variable date=" " genommen, da wir am Anfang die zu berechnende Variable als ,,dates" eingegeben haben und es nicht genau diesselbe sein darf, da PyCharm sonst die Fehlermeldung ,,shadowing" meldet, die bedeutet, dass man die Variable nicht nochmal verwenden darf.
Nun kam der letzte Befehl, ,,print" und hier muss wieder die Anfangsvariable rein, damit er den Vorgang abspult, den wir ihm programmiert haben, also ,,findday(date)", so hatten wir ,,print(findday(date))". 
Wenn man nun bei date=" " zwischen die doppelten Strings ein Datum tippt (ohne Punkt), also z.B. date = "24 03 2023", dann errechnet er einem den Wochentag, hier wäre es Freitag.


