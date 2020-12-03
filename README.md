# Projektseite: "Enqui"

## Inhaltsverzeichnis 

[1. Einleitung](#Einleitung)

[2. Spielidee](#Spielidee)

[3. Screens](#Screens)

[4. Funktionen](#Funktionen)

[5. Buttons](#Buttons)

[6. Inhalt des Quiz](#Inhalt)

[7. Spielende](#Spielende)

[5. Schlusswort](#Schlusswort)

## Einleitung<a name="Einleitung"></a>

Im ersten Halbjahr des 12. Jahrgangs haben wir im Rahmen des Informatikunterrichts das Englischquiz "Enqui" erstellt. Dazu haben wir die Seite code.org und dessen Funktion AppLab verwendet, da diese für Anfänger im Programmieren ausgelegt ist. Da dieses Programm mit Bausteinen arbeitet, bot es sich für uns an, da wir keinerlei Vorkenntnisse in Informatik hatten. Nachdem wir uns die Einführungsvideos zu AppLab angesehen haben, waren wir froh, ein solches Anfängerprogramm gefunden zu haben, mit welchem das Projekt und die Anforderungen an dieses erfüllbar wirkte. 

Dabei haben wir uns dazu entschieden, ein Quiz zu machen, da dies mithilfe der Funktionen des Programms gut realisierbar und gleichzeitig mit unseren Kenntnissen machbar erschien. 

## Spielidee<a name="Spielidee"></a>

"Enqui" ist ein Englischquiz für Anfänger, welches aus zehn verschiedenen Fragen besteht. Es gibt unterschiedliche Fragentypen: Vokabel- und Grammatikfragen und Fragen anhand von Bildern und Geräuschen. Dabei gibt es ein Punktesystem, welches auch in den Minusbereich reicht und für jede Frage einen (Minus)Punkt bringt. Das Quiz ist gewonnen, wenn man von den zehn Fragen mindestens sechs richtig beantwortet, also sechs Punkte erreicht hat.

## Screens<a name="Screens"></a>

Für die Screens haben wir die Funktion der Screengestaltung bei AppLab genutzt, bei der man den Aufbau der Screens nicht im Code verankert, sondern diese gesondert anlegen und gestalten kann. Zur Verbindung der einzelnen Screens miteinander werden Buttons und Funktionen gebraucht. 

Das Englischquiz besteht aus insgesamt 13 Screens, wobei es einen Startscreen, welcher beim Öffnen des Quiz gezeigt wird, zwei Endscreens, wovon einer beim Erreichen der Mindespunktzahl (bei einem Gewinn) und der andere beim Nichterreichen (bei einer Niederlage) gezeigt wird und zehn Fragescreens, auf welchem sich die unterschiedlichen Fragen befinden, gibt.  

https://github.com/Emmax0203/Projektseite---Enqui/blob/main/Informatik.png
https://github.com/Emmax0203/Projektseite---Enqui/blob/main/Informatik1.png
https://github.com/Emmax0203/Projektseite---Enqui/blob/main/Informatik2.png

## Funktionen<a name="Funktionen"></a>
Zur Vereinfachung und Verkürzung unseres Codes haben wir einige allgemeine Funktionen erstellt, um bei gewissen Ereignissen, bestimmte Reaktionen hervorzurufen. Dabei gibt es eine für richtige Antworten:

function right() {
 playSound("sound://category_achievements/lighthearted_bonus_objective_1.mp3", false);          bestimmt den Sound, der bei richtigen Antworten gespielt wird
  Anzahl = Anzahl + 1;                                                                          addiert die Punkte, bei richtiger Antwort
  setText("Punktetafel", "Punkte = " + Anzahl);                                                 zeigt den neuen Punktestand an
  }
  
  und eine für die falschen Antworten:
  
  function wrong() {
  playSound("wrong.mp3", false);
  Anzahl = Anzahl - 1;
  setText("Punktetafel", "Punkte = " + Anzahl);
  }
  
  Außerdem gibt es eine Funktion für die Endscreens:
  
function endGame() {
  if (Anzahl < 6) {                                                                             beschreibt die Weiterleitung zum negativen Screen
    setScreen("screen11");
  } else {                                                                                      beschreibt die Weiterleitung zum positiven Screen
    setScreen("screen12");
  }
}

Zusätzlich gibt es ein funktionierendes Scoreboard, das durch die Variable "Anzahl" festgelegt und verändert wird. Dieses taucht auf allen Screens auf und zeigt den momentanen Punktestand an. 

## Buttons<a name="Buttons"></a>

Bei unserem Quiz haben wir Buttons verwendet, mit welchen man zu dem nächsten Screen gelangt und Events, wie Punkte und Sounds auslöst. Dabei gibt es die Buttons A, B und C, denen dann diese verschiedenen Funktionen (wrong, right) zugeordnet sind. Des Weiteren haben wir eine interaktive Seite (Startseite) erstellt, bei der man durch klicken auf einen beliebigen Punkt der Seite auf den ersten Screen gelangt.  

## Inhalt des Quiz<a name="Inhalt"></a>

Das Thema unseres Quiz ist Englisch für Anfänger. Somit sind die Fragen einfach gehalten und gehen nur auf Grundkenntnisse ein. Hierbei gibt es verschiedene Fragentypen: Vokabellernen durch Verknüpfung von Bild und englischem Wort, Geräusch und Wort und englischem Wort mit Übersetzung. Des Weiteren gibt es Grammatikfragen, wobei deutsche Sätze ins Englische übersetzt werden sollen. Diese Fragen haben wir uns alle selbst ausgedacht. Außerdem ist das Quiz ein multiple-choice Quiz mit jeweils drei Antwortmöglichkeiten (A, B, C).  

## Spielende<a name="Spielende"></a>
Das Spiel endet, wenn der Spieler alle zehn Fragen des Quiz beantwortet hat, unabhängig von dem derzeitigen Punktestand. Durch den Punktestand wird lediglich entschieden, auf welchen der beiden Endscreens der Spieler am Ende weitergeleitet wird. 
Dazu gibt es eine endGame-Funktion, die mithilfe der if-else-Schleife von AppLab bestimmt, welcher der beiden Screens am Ende des Quiz angezeigt werden soll. In dieser ist festgelegt, dass, wenn (if) die Anzahl unter sechs Punkten ist, der negative Endscreen angezeigt wird und ansonsten (else) der positive Screen angezeigt wird. Auf den letzten beiden Screens (Endscreens) kann man außerdem das Quiz restarten und von vorne beginnen. 

## Schlusswort<a name="Schlusswort"></a>
Schlussendlich sind wor mit unserem Projekt sehr zufrieden, da wir bis vor einigen Monaten noch nie programmiert haben und keinerlei Informatikkenntnisse besaßen. Auch wenn es einige Schwierigkeiten gab, habne wir so gut es geht Lösungen gefunden und unser Quiz Schriit füt Schritt weiter aufbessern können. Die Kenntnisse haben wir uns größtenteils über Videos und Eigenarbeit, sowie viel Probieren angeeignet, weshalb es für uns von besonderer Bedeutung ist. Dabei hatten wir vor allem Probleme mit dem Scoreboard und mit der Vereinfachung unseres Codes, wofür aber zum Glück am Ende Lösungen finden konnten, mit denen wir auch zufrieden sind. 
