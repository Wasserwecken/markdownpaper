<!-- REFERENCES -->
[The19thcenturypostcards]: https://rarehistoricalphotos.com/french-postcards-futuristic-world-year-2000/
[HyperloopHistory]: https://www.businessinsider.com/history-hyperloop-pneumatic-tubes-as-transportation-2017-8
[EssentialPapers]: https://www.reddit.com/r/learnmachinelearning/comments/1dx7kvr/essential_ml_papers/
[Flocking]: https://en.wikipedia.org/wiki/Flocking
[OpenDataSets]: https://github.com/Zjh-819/LLMDataHub
[DatasetRLHF]: https://huggingface.co/datasets/Anthropic/hh-rlhf/viewer/default/train?views%5B%5D=train&row=0
[DatasetSFT]: https://huggingface.co/datasets/HuggingFaceH4/no_robots/viewer/default/train?views%5B%5D=train&row=15


<!-- CONTENT -->
# (H4) KI unter der Haube - Wie funktioniert ein LLM?
Als Künstliche Intelligenz (KI) werden Systeme bezeichnet die Probleme und Aufgaben lösen können die menschliche Intelligenz benötigen oder diese sogar übersteigen. Solche System können aus riesigen Datenmengen Muster erkennen um Vorhersagen zu erzeugen oder Inhalte zu generieren. Künstliche Intelligenz ist heute so etwas wie die Industrielle Revolution, nur eben für die Verwaltung und Steuerung.

Das Thema der Künstlichen Intelligenz $a = b$ gibt es bereits seit den 50er Jahren. Allerdings waren das alles aber nur theoretische und mathematische Konzepte. Mit den 2000er Jahren kam das Internet in der Gesellschaft an, und die ersten Datenmengen. [sail] Auch die Leistung der Computerhardware wurde mit jedem Jahr leistungsstärker so dass die frühen Konzepte tatsächlich Anwendbar und Wirtschaftlich wurden. Das Interesse die Forschung, und die Ausbildungen dahin sind seit jeher angestiegen und es gab immer neue Durchbrüche, wie z.B. neuronale Netze. Und seit 2020 / 2021 hat es die Aufmerksamkeit der breiten Bevölkerung, angestoßen durch die Veröffentlichung von ChatGPT und DALLE durch OpenAI. Auf einmal konnte jeder ohne technischen Vorkenntnisse Text und Bilder generieren, nur durch die Eingabe von ganz normalem Text, auch natürliche Sprache genannt. Die Möglichkeit das System natürliche Sprache erst seit kurzem verarbeiten und verstehen können.

<ref>
<img src="./.doc/sailboat.bmp"/>
<refInfo id="sail" type="figure" />
Als Künstliche Intelligenz (KI) werden Systeme bezeichnet die Probleme und Aufgaben lösen können die menschliche Intelligenz benötigen oder diese sogar übersteigen.
</ref>

$$\pi^* = v_{\pi^*}(s) = \max_{a \in A} \sum_{s',r} p(s',r|s,a) [r+\gamma v(s')]$$

## Bullshit Bingo
Kaum eine Software wird momentan ohne integrierte "KI"-Funktion beworben. Überall werden Chat-Assistenten beworben und auch teils kostenlos angeboten. Nahezu jede Softwarefirma hat einen Blogeintrag über KI und maschinelles Lernen. Denn alles wird besser, schneller, effizienter, produktiver und genauer mit Neuronalen Netzten, LLM's, KI-Agenten und maschinellem Lernen. Bei all diesen Angeboten und Schlagwörter ist es schwierig zu erkennen was genau KI in Produkten macht und ob KI überhaupt einen Mehrwert für die eigene Produktivität bieten kann.

Dabei hat KI Ihre Berechtigung und kann extrem hilfreich sein. Aus vielen Bereichen wie z.B. Bilderkennung und Big Data ist sie kaum noch weg zu denken. Mit neuronalen Netzten können Muster in riesigen Datenmengen erkannt und erlernt werden um so Röntgenbilder besser zu erkennen oder genauer das Wetter vorhergesagt werden. Nur laufen diese Anwendungen versteckt im Hintergrund oder im industriellen Rahmen, unsichtbar für den letztendlichen Verbraucher. Die KI-generierten Inhalte mit denen wir immer mehr konfrontiert werden ist nur die Spitze des Eisberges.



#### Hierarchische Einordnung
Die Begrifflichkeiten die im Marketing sind sie vielen Menschen die nicht aus dem Bereich der Informatik kommen gänzlich oder nur oberflächlich bekannt. Im folgenden werden wichtige Konzept und Begriffe erklärt und was dahinter steckt, zwar nicht im Detail und in der Tiefe aber doch soweit ohne ein Informatikstudium voraus zu setzten.

![Künstliche Intelligenz ist nur der Überbegriff für alles, und viele Begriffe sind miteinander verbunden.](./mat/1.hierarchy.png)


**Künstliche Intelligenz (KI)** ist der Überbegriff für Systeme die Aufgaben meistern und dabei 'intelligent' wirken. Es gibt keine eindeutige Definition was eine künstliche Intelligenz als solche auszeichnet. Was wiederum bedeutet das auch einfache Wenn-Dann-Bedingungen ausreichen können, um ein System als Künstliche Intelligenz zu betiteln. Der Begriff definiert auch nicht, ob ein System in der Lage ist, selbständig zu lernen. Somit kann fast alles als KI betitelt werden, von den einfachsten Tricks bis hin zu den komplexesten neuronalen Netzen. Z.B. Die Routenplanung in Google Maps, Die ersten Schachcomputer oder Outlook-Regeln die Emails sortieren oder eben ChatGPT, DALL-E und VEO3.

![Sowie die Routenplanung von Google Maps als auch einfache Schachcomputer basieren auf 'intelligente' Such-Algorithmen.](./mat/1.classicAI.png)


**Maschinelles Lernen (ML)** umfasst alle Systeme die aus Daten lernen und sich an Aufgaben adaptieren, ohne dabei explizit programmiert zu werden, Sie lernen ausschließlich anhand von Beispieldaten. Anstatt statischer Regelungen folgen Sie dem Prinzip "Lernen durch Beispiel", durch Analyse großer Datensätze (Supervised Learning), Entdeckung von Strukturen (Unsupervised Learning) oder Optimierung von Entscheidungen (Reinforcement Learning). Dabei sind die Daten für das Training ein fundamentaler Punkt: Die Leistungsfähigkeit und Zuverlässigkeit eines solcher Systeme stehen und fallen mit der Qualität und Menge der Daten, die zum Lernen zur Verfügung stehen.

![Von Links nach Rechts: k-NearestNeighbour, Classifizierung, Regression. Durch das Training können Grenzen gezogen werden oder Ähnlichkeiten abgeschätzt werden.](./mat/1.classicML.png)


**Neuronale Netzte (NN)** sind ein Teilgebiet des maschinellen Lernens und beschreiben Art von Algorithmen deren Struktur von biologischen Neuronen inspiriert wurden. Allerdings hören die schnell Ähnlichkeiten auf, denn unser Hirn und ein Neuronales Netz haben im Detail kaum etwas gemein. Haben Anwendungsfälle zu viele Parameter von denen das Ergebnis abhängt kommen klassische ML-Algorithmen schnell an Ihre Grenzen, und auch die Aufbereitung der Daten kann eskalieren. Das besondere an neuronalen Netzen ist das Sie sich selbstständig optimal aus den Daten lernen können, was die Entwicklung und Anbindung solcher Netzwerke erheblich erleichtert. Sobald solch ein Neuronales Netz trainiert wird spricht man von Deep Learning (DL). Allerdings haben neuronale Netze einen erheblich höheren Rechenaufwand und die Nachvollziehbarkeit von falschen Ausgaben ist nicht mehr gegeben.

![Schematischer Aufbaue eines neuronalen Netzten das darauf trainiert werden kann Tiere in einem Bild zu erkennen.](./mat/1.dnn.png)

**Generative AI** Generative AI bezieht sich auf KI-Systeme, die in der Lage sind, neue Inhalte zu erstellen, indem sie aus existierenden Daten lernen. Diese Systeme können Texte, Bilder, Musik, Videos und andere Medien generieren, die ähnlich wie die trainierten Datensätze sind. Ein Beispiel für eine generative AI ist DALL-E, das Bilder aus Textbeschreibungen erzeugen kann. Diese "kreative" Fähigkeit, Neues zu generieren, unterscheidet sie grundlegend von anderen KI-Modellen die entwickelt wurden um eine Aufgabe immer gleich und mit einem präzisem Ergebnis zu lösen.

![Ein Bild das vollständig durch ein Modell generiert wurde. Ob fotoreal oder surreal spielt keine Rolle, auch als Motive kann alles Erdenkliche erzeugt werden.](./mat/1.genAI.webp)

**Large Language Models (LLMs)**, oder auch große Sprachmodelle, sind eine spezielle Art von neuronalen Netzen, die darauf Trainiert sind natürliche Sprache als Eingabe anzunehmen und als Ergebnis wieder natürliche Sprache Auszugeben. Auch zählen Sie zu den generativen KI's da es auf Fragen oder Aufgaben in natürlicher Sprache nicht nur eine Möglichkeit für die Antwort gibt, sondern die Korrektheit erst durch die Semantik ergibt. Um diese Modelle handelt sich all nachfolgender Inhalt, weil eben diese Modelle, bzw. die Möglichkeit natürliche Sprache automatisiert zu verarbeiten unendlich viele neue Optionen bietet.

![Large Language Models verstehen unsere natürliche Sprache, und können auch so wieder antworten. Dadurch kann man sich ohne technisches Vorwissen wie mit einem anderen Menschen unterhalten.](./mat/1.llm.png)


#### Generalisierung
Generalisierung beschreibt die Fähigkeit ob und wie gut Modelle auf unbekannte Daten reagieren können. Der Begriff stammt aus dem maschinellem Lernen und beschreibt die Kernidee. Ein Algorithmus soll aus bestehenden Daten (Trainingsdaten) Mustern erkennen und korrekte Vorhersagen treffen. Der eigentlich Mehrwert der durch das Training entsteht ist, das dieser Algorithmus dann auf Daten und Situationen angewendet werden kann die es noch nie gesehen hat, also nicht teil des Trainings war, aber trotzdem korrekte Vorhersagen und Ausgaben erzeugt.

In den meisten Fällen ist es unmöglich alle Eventualitäten eines Problems zu erfassen. Z.B. gibt es in Schach ungefähr 10^40 mögliche Stellungen und beim Autofahren es gibt unendlich viele Einschlag Winkel eines Lenkrad. Deswegen ist die Aufgabe von ML-Algorithmen mit wenigen Parametern die gesamte Problemstellung abzubilden. Im Umkehrschluss bedeutet das aber auch das ein Algorithmus nie Fehlerfrei sein kann, und alle Ergebnisse eine Schätzung / Annäherung sind.

![Das große Ziel vom maschinellen Lernens, anhand der Trainingsdaten lernt das Modell Muster und Ähnlichkeiten.](./mat/1.generalisation.png)

Das Ergebnisse einer KI immer nur Schätzung sind hört sich im ersten Moment dramatisch an, kann aber völlig in Ordnung sein. Wir sind in unserem Alltag ständig mit Schätzungen statt exakten Werten konfrontiert. Fahrzeiten werden geschätzt, beim Kochen wird nicht alles genau auf das Milligramm abgewogen und in der Buchhaltung gibt es Rundungsfehler. Und auch in der Industrie gibt es definierte Toleranzen für Größen, Temperaturen oder Reinreiten. Wenn also KI's mit ihren Schätzungen so gut sind, das deren Fehler tolerierbar sind, erzeugen Sie einen Mehrwert. Bei generativen KI's spricht man aber weniger von "Fehler" wenn diese eine fehlerhafte Ausgabe erzeugen, sondern von "Halluzinationen" oder "Artefakte".



#### Daten Daten Daten
Damit nun ein Algorithmus selbstständig lernen kann benötigt er "Beispiele" was oft einfach als "Daten" bezeichnet wird. Die Menge und Qualität dieser Beispiele sind dabei enorm wichtig, und im optimalen Fall hat man Unmengen in bester Qualität davon. Hier kann man eine Analogie zu uns Menschen aufbauen, je besser ein Unterricht vorbereitet ist und der Lehrende sich sicher im Thema ist, desto besser können Lernende daraus Schlüsse und Wissen gewinnen.

Warum die Qualität der Daten wichtig ist, ist schnell zu Erklären. Wie bei uns Menschen können wir nur aus Erfahrungen und Informationen lernen die in sich schlüssig und vollständig sind. Würde jedes zweite Wort in einem Wikipedia- oder Zeitungsartikel fehlen, könnten wir kein oder nur mit größten Schwierigkeiten Wissen daraus zu ziehen. Äußerem dürfen sich die gegebenen Informationen nicht widersprechen, da weder wir Menschen noch ein Algorithmus dann entscheiden kann was die richtige Information ist. Deshalb sind Daten nicht immer gleich Daten. Sie müssen zuerst immer analysiert und dann aufbereitet werden bevor ein System trainiert werden kann.

Die Menge der Daten zum Lernen ist deshalb relevant, da diese indirekt den Umfang der Problemstellung abbilden. Das bedeutet das eine ML-Algorithmus nur dann eine gute Vorhersage treffen kann wenn es beim Training schon einmal mit etwas ähnlichem Konfrontiert wurde. Wenn also eine Problemstellung viele Ausnahmen oder Fallunterscheidungen besitzt, sollten diese auch im Trainingsdatenset enthalten sein. Bei uns Menschen verhält es sich genau gleich, wenn ein Schreiner viele Möbelstücke in jeglichem Stil sauber fertigen können möchte, muss er sich dabei auch jedem Stil und Möbelstück probiert haben. Andernfalls kann das Ergebnis Minderwertig oder nicht ausreichend sein.

Wenn nun ein System natürliche Sprache erzeugen soll braucht es dabei extrem viel Beispiele wir mit Sprache sehr viel Informationen übermitteln können. Dazu kommt das die gleiche Informationen in unendlich vielen Variationen übergeben werden kann, z.B. in verschiedenen Sprachen oder Formulierungen. Und gleichzeitig ist Kontext für natürliche Sprachen extrem wichtig, da die gleichen Wörter oder Formulieren komplett unterschiedliche Bedeutungen je nach Kontext haben können.



#### Grafikkarten
Grafikprozessoren, besser bekannt als GPUs (Graphics Processing Units), zeichnen sich besonders durch ihre Fähigkeit aus, eine große Anzahl derselben einfachen Berechnungen gleichzeitig durchzuführen. Ihre ursprüngliche Aufgabe war die schnelle Darstellung von Computergrafiken, bei der die Eigenschaften (wie Farbe oder Position) vieler einzelner Bildpunkte, der Pixel, zeitgleich berechnet werden müssen. Anwendungen im Bereich der Künstlichen Intelligenz (Training und Inferenz), profitieren enorm von dieser Architektur. Allen voran neuronale Netze, bestehen im Wesentlichen aus einer Vielzahl von Multiplikationen und Additionen, die als Matrizenoperationen zusammengefasst werden. Obwohl diese Berechnungen auch auf herkömmlichen Hauptprozessoren (CPUs) durchgeführt werden können, sind GPUs aufgrund ihrer Vielzahl an spezialisierten Recheneinheiten (Kernen) um ein Vielfaches schneller und effizienter für das Training und die Ausführung von KI-Modellen als CPUs.

![Grafikarten Chips sind dafür optimiert einfache Rechenoperationen parallel auszuführen.](./mat/1.cpugpu.png)


## Large Language Models
LLMs stellen einen bedeutenden Fortschritt im Bereich der Sprachverarbeitung dar der als Natural Language Processing (NLP) bezeichnet wird. Ihre Fähigkeit liegt darin, natürliche Sprache nicht nur lesen zu können, sondern diese auch als Ergebnis zu erzeugen. Sie sind in der Lage, mit der Komplexität, den Ungenauigkeiten und den feinen Nuancen menschlicher Kommunikation umzugehen. Das revolutionäre daran ist, dass LLMs völlig neue Wege eröffnen, wie Menschen und Computer miteinander interagieren können, indem sie die menschliche Sprache als intuitive Schnittstelle nutzen. Dadurch können sie eine Vielzahl von Aufgaben erfüllen, von der Beantwortung komplexer Fragen über das Zusammenfassen langer Texte bis hin zur Erstellung kreativer Inhalte oder sogar Programmiercode, alles durch die Interaktion in natürlicher Sprache.



#### Funktionsweise
Das erste was passieren muss damit ein LLM Text verarbeiten kann ist die Umwandlung des Textes in Zahlen. Das muss ständig sowohl beim Training als auch bei der Ausführung jeden Prompts's geschehen. Den Neuronale Netzte und ML-Algorithmen im allgemeinen funktionieren ausschließlich mit Kommazahlen, und nur so können GPU und CPUS die Ausgabe berechnen für die ein Model trainiert wurde. Dabei ist die Ausgabe allerdings auch wieder nur eine Zahl, und diese muss wieder in Text umgewandelt werden.

Die Umwandlung von Text in Zahlen erfolgt durch die "Tokenizing". Hierbei wird Text in eindeutige Silben zerlegt, und diese Silben wiederum sind nummeriert. Diese Silben werden als "Token" bezeichnet sind aber keine Silben wie Sie kennen sondern haben Ihren einen Katalog in dem Sie definiert werden, OpenAI nutzt z.B. für die neueren Modelle 200.000 unterschiedliche Tokens. Diese Menge an Tokens erscheint auf den ersten Blick als viel, aber ist eine viel kleinere Menge als wenn man jedes Wort jeder Sprache durchzählen würde und Rechtschreibfehler fallen weniger ins Gewicht. Nachdem ein Text in Tokens zerlegt wurde kann er einem LLM übergeben werden, genauso wie die Ausgabe eines LLM's wieder eine folge von Tokens ist die wieder in für uns lesbaren Text umgewandelt werden kann.

![Ein Satz wird in vordefinierte Tokens zerlegt, jedes Token hat seine eigene Id, die wiederum einen eigenen Vektor besitzt mit dem dann letztendlich ein LLM als Eingabe rechnen kann.](./mat/2.tokens.png)

Die eigentliche Verarbeitung und sozusagen "Magie" wie diese Tokens miteinander verrechnet werden ist sehr kompliziert und setzt stabile mathematische Kenntnisse voraus. Nichtsdestotrotz kann die Idee hinter allen Berechnungen grob verallgemeinern werden: Ein einzelnes Wort für sich genommen hat wenig bis keinen Informationsgehalt, erst wenn diese in Sätzen oder Paragrafen kombiniert werden entstehen Informationen, was als Kontext bezeichnet wird. Je nach Wort kann seine Bedeutung je nach Kontext komplett verändern, z.B. kann eine "Bank" eine Sitzgelegenheit oder ein Finanzinstitut bezeichnen. Das Ziel aller Operationen ist nun für jedes Wort die Beziehungen zu den anderen Wörtern zu finden, und auch zu diesen Beziehungen die Beziehung zu den anderen Beziehungen zu finden, und das aber tausendmal wiederholt. So können LLM's Sinn und Informationen aus Texten gewinnen.

![Abstrakte Sicht auf die Beziehungen die ein LLM intern bildet.](./mat/2.attention.png)

Wie wird aber die Ausgabe erzeugt, also ein vollständiger Text generiert? Das passiert nicht auf einen Schlag, also nicht Tokens rein und Tokens raus. Der Trick den LLM verwenden ist das Sie so lange das nächste Token vorhersagen bis ein vollständiger Text entsteht, ähnlich wie in einem Lückentext bei dem das letzte Wort im Satz fehlt. D.h. das Ergebnis eines LLMs ist ein einzelnes Token, nicht mehr und nicht weniger. Dieses einzelne Token wird dann der Eingabe hinzugefügt, und wieder dem LLM übergeben um wieder das nächste Token vorherzusagen, was wieder der Eingabe hinzugefügt wird. Das passiert so lange bis das LLM als Token ein "EOS" ausgibt, also ein Token das für "EndOfSequence" bzw. "Ich bin fertig" steht. Diesen Vorgang kann man sehr gut bei vielen Chats wie ChatGPT beobachten, das erscheinen einzelner Wörter nach und nach ist keine Design-Entscheidung sondern einfach der aktuelle Stand der LLM beim erzeugen der Ausgabe.

![Ein Sprachmodell versucht nur das nächste Token vorherzusagen, immer und immer wieder bis eine vollständige Antwort entsteht.](./mat/2.pred.png)

Eine letzte Anmerkung muss noch zur Art der Vorhersage des letzten Tokens gemacht werden. Eine LLM gibt nicht einfach die Nummer eines Token als Antwort, sondern eine Wahrscheinlichkeitsverteilung für alle 200.00 Tokens im Wörterbuch. Dies Ausgabe kann also eher als eine Auflistung von Wörter verstanden werden die jetzt wahrscheinlichsten sind um den Text fortzuführen. Das ermöglich Nutzern die Ausgabe von LLM in seiner Kreativität zu steuern.



#### Training
Die Eigentliche Frage die sich aber stellt ist: Woher weiß ein Modell in welche Bedeutung Tokens, Wörter und Beziehung sie untereinander haben? Bei ML-Algorithmen die keine neue Inhalte wie Bilder oder Text generieren ist das Prinzip einfacher zu erklären. Wären dem Training wird dem Model zum einen die Eingabe übergeben, und erzeugt darauf hin eine Ausgabe und diese wird dann mit einem erwartetem Wert verglichen. Wenn dieser nicht passt wird dem Model "auf die Finger gehauen" und es korrigiert wird seine Parameter um nächstes mal näher am erwartetem Ergebnis zu liegen. Ähnlich wie bei uns Menschen, wenn wir irgendwann mal auf eine heiße Herdplatte, heiße Kohlen und in eine Flamme gefasst haben verstehen wir irgendwann das Konzept "Hitze" und das zu viel davon uns nicht gut tut. Ein anderes Beispiel ist das Training von Tieren, die Leckerlies bekommen wenn Sie etwas richtig gemacht.

Das Training von LLM ist aber komplex, mehrstufig die genauen Methoden und Trainingsdaten nicht immer veröffentlicht. Aber grob kann das Training in zwei Phasen eingeteilt werden. Als erstes beginnt das sogenannte "Pre-Training", bei dem die LLM grundlegend natürliche Sprache lernt und versteht. Dabei lernt ein Model ganz stupide einfach nur das nächste Token vorherzusagen. Es wird eine Unmenge von Texten aus Büchern, Artikeln und Forenbeiträge, Chats und Dialoge präsentiert und muss von Ausschnitten das nächste Token vorhersagen. Z.b wird die erste Seite eines Buchs übergeben und muss das nächste Token auf der folge Seite vorhersagen.

![Einzelnes Beispiel für das Finetuning damit ein LLM auf Fragen und Anweisungen reagieren lernt.](./mat/2.dataset1.png)

Ist die erste Phase abgeschlossen kann ein LLM tatsächlich schon Text verarbeiten, sinnvolle Ausgaben erzeugen und einfachen Anweisungen folgen. Diese Modelle dienen als Basis für spezialisierte Modelle. Die nächste Phase ist die Spezialisierung auf eine Aufgabe, Verhalten oder Wissen. So werden  Modelle mit zusätzlichen Beispielen weiter trainiert um z.B. besser Anweisungen zu folgen oder sich glaubhafter mit Benutzern zu chatten. Außerdem werden LLM oft in der Phase noch kontroverse Themen abtrainiert, so das Unterhaltungen zu z.B. Drogen, Gewalt und Sexualität kaum möglich sind.

![Auch wir Benutzer erzeugen für die Dienstleister unbewusst Trainingsdaten. Durch die Auswahl der besseren Antwort wird ein Model später darauf getrimmt.](./mat/2.rlhf.webp)

Die erste Phase ist dabei die teuerste, da Unmengen von Text benötigt werden, eben um alle Facetten aller Sprachen und Situationen abbilden zu können. Allein GPT-3 wurde mit ca. 500 GB reinem Text gefüttert, und das Training dauerte zwar "nur" 34 Tage weil es auf 1024 GPU's verteilt wurde, und kostete $4-6 Millionen. Die zweite Phase des Trainings ist nicht zu unterschätzen, ist aber um ein vielfaches kürzer. Online findet man viele Datensets da die Forschung um dieses Thema explodiert ist, und bietet einen Einblick was genau ein Sprachmodell so zu lernen hat.

Was aber vielleicht die Größte Unterscheidung zu uns Menschen und Sprachmodellen ist: Deren Wissen und Lernprozess hört nach dem Training auf. Sprachmodelle haben nur Informationen über Dinge die Ihnen gezeigt wurden, d.h. was heute in der Welt passiert ist kann ein LLM nicht wissen. Nach dem Training bleiben die Parameter eines Modells "eingefroren", auch Die Ausführung des Modells verändern diese nicht. Modelle sind also nicht in der Lage nach dem Training sich "weiter zu entwickeln", anders wie wir Menschen, die Täglich und Stündlich reflektieren oder lernen, sowohl unterbewusst als auch bewusst.


#### Eingaben
Im Prinzip übergibt man einem LLM einen Text als Eingabe und bekommt wiederum einen Text zurück. Für die Übergabe gibt es zahlreiche Einstellungen um Einfluss darauf zu nehmen was genau an Text erzeugt werden soll. Und leider gibt es auch eine wichtige Einschränkung: Die Menge an Text die ein LLM verarbeiten kann (*Context Length*) ist je nach Model unterschiedlich. GPT-3 was 2020 vorgestellt wurde hatte ein Limit von 2048 Token, und GPT4o was 2024 vorgestellt wurde schon 128.000 Tokens. Die 30 Artikel der Menschenrechte umfassen auf Englisch ~1700 Tokens und auf Deutsch ~2400 Token und das erste Harry Potter Buch in englischer Sprache entspricht ungefähr 128.000 Tokens. Neben einem Text gibt es mittlerweile noch mehr Eingaben mit denen LLM's umgehen kann, letztendlich wird aber alles in Tokens umgewandelt. Text ist aber nach wie vor die Grundlage für Modelle um die sich alles dreht.

![1. Der Kontext kann sich aus dem bisherigen Chatverlauf, Tools die zu verwenden sind und oder Bilder zusammen setzten. 2. Wenn ein Tool benutzt werden soll wird dieses von der LLM ausgerufen. 3. Das Sprachmodell generiert dann die Antwort](./mat/2.inputs.png)

##### Prompting
Die Eingabe von Text (Prompt) ist aber nicht gleich Text für LLM's. Die Modelle wurden darauf trainiert das es unterschiedliche Arten von Text gibt und wie das Model darauf zu reagieren hat. Insgesamt gibt es drei Arten:
- *User-Prompt*: Das ist die eigentliche Nutzereingabe und Anweisung für das Modell. Ein guter User Prompt ist präzise und gibt Kontext.
- *Assistant-Prompt*: Das sind die generierte Antworten des  Sprachmodells auf die vorhergehenden User-Prompts.
- *System-Prompt*: Das beschreibt das grundlegende Verhalten, Kontext und Richtlinien für das Sprachmodell, bevor es Benutzereingaben erhält.

Alle Prompts zusammen ergeben den vollständigen Text der übermittelt wird. Dieser Text bestimmt maßgeblich wie und was das Sprachmodell antwortet. Außerdem können hier Informationen übermittelt werden auf die das LLM während des Trainings keinen Zugriff hatte (Firmen interne Dinge oder aktuelle News). Das macht aber nur Sinn wenn die zusätzlichen Informationen bei der Beantwortung der Frage helfen.

![Beispiel eines Chats mit System-Prompt. Man erkennt an den Antworten des LLMs das der Systemprompt sehr stark die Antworten steuert. AAußerdem werden alle Nachrichten im Chat als Kontext (User u. Assistant prompt) mitgegeben.](./mat/2.chat.png)

##### Tooling
Eine weitere Information die einem LLM übergeben werden kann sind 'Tools'. Das sind Funktionsaufrufe um entweder Aktionen anzustoßen oder Daten zu lesen (Kalender updaten oder auslesen, Email versenden oder eine Suche ausführen). Dabei kann die LLM selbst entscheiden ob und mit welchen Parametern sie ein 'Tool', also Funktionsaufruf, ausführen möchte um die Eingabe des Benutzer zu beantworten oder zu erfüllen. Diese Eigenschaft, selbstständig zu entscheiden was jetzt getan werden muss, kann einem Workflow gleich gesetzt werden, bei dem nicht mehr der Programmierer definiert wann was wie passiert, sondern die LLM nimmt das selbst in die Hand nimmt. Somit kann ein LLM mit allen möglichen Funktionen ausgestattet werden ohne das alle ausgeführt müssen, wie ein Sekretär der Anfragen annimmt verarbeitet und entscheidet was weiter zu tun ist.

##### Multimodal
Durch Forschung und Weiterentwicklung können einige Modelle nicht nur Text verstehen, sondern auch andere Medien wie Bilder können als Eingabe mitgegeben werden. Wenn ein LLM nicht nur auf Text bei Eingabe und Ausgabe beschränkt ist, spricht man von 'Multimodal', was bedeutet dass ein LLM neben Text andere Medien akzeptiert und oder erzeugen kann. Momentan liegt der Fokus der Entwicklung mehr auf die Eingabe von unterschiedlichen Medien, es gibt aber bereits Arbeiten an LLM's die neben Text auch andere Medien wie z.b. Video ausgeben können. Das analysieren von Medien ermöglicht nochmal eine neue Dimension der Flexibilität von LLM's. Es gibt das Sprichwort 'Ein Bild sagt mehr als 1000 Worte', ein Bild ist eben eine komplett andere Form gegeben über Text, wie Informationen festgehalten werden. Somit können LLM's auch von Bilder den Inhalt, Emotionen oder Rückschlüsse ziehen.



### Ausgaben
Neben den Möglichkeiten der Eingabe gibt es auch Optionen die Ausgabe explizit zu steuern. Diese sind zwar nicht so vielseitig, aber dennoch ausschlaggebend für die Spezialisierung für gewisse Aufgaben. Je nach Einsatz einer LLM sollten hier Anpassungen vorgenommen werden um bessere und verlässlichere Ziele zu erreichen. Für LLMs die im Hintergrund agieren ist es vorteilhafter wenn deren Ausgaben nachvollziehbar und deterministisch sind.

#### Structured Output
Wenn ein LLM nicht als Chat-Bot eingesetzt wird, ist meistens eine Anforderung das die Antworten des LLM's in einem bestimmten Format oder Sektionen zurück kommen. Zwar kann dem LLM im Prompt mit übergeben werden wie die Antwort zu formatieren ist, z.b. Betreff und Inhalt bei einer Email, allerdings ist nicht sicher gestellt das diese Antwort auch genau so erscheint. Mit 'Structured Output' zwingt man eine LLM dazu die Antwort in ein vordefiniertes Schema zu pressen. Das ist vor allem dann praktisch wenn die AAusgabe automatisiert weiter geleitet werden soll, also z.b. in eine Excel-Liste oder Datenbank.

#### Settings
Neben dem 'Structured Output' gibt es viele weitere Regler die die Ausgabe beeinflussen. Diese bestimmen wie das nächste Token vorhergesagt wird.Ein wichtiger Parameter ist *Temperature*, sie beeinflusst wie 'kreativ' oder 'zufällig' die Token-Vorhersage des Modells ist. Eine höhere Temperatur führt zu kreativeren, aber potenziell abschweifenden Antworten. Eine niedrige Temperatur für zu eher gleichen, nüchternen aber genaueren Antworten. Neben der Temperatur gibt es noch *p-Sampling*, *Frequency Penalty*, *Max Length*, usw. Diese sind entweder selbst erklärend oder haben ähnliche Auswirkungen wie *Temperature*. An diesen Parametern muss man aber nur selten Anpassungen vornehmen.





## Anmerkungen
Die technischen Grundlagen von LLMs und KI im generellen sind wichtig, aber sie zeigen nicht die Möglichkeiten und Konsequenzen auf die Sie mit sich bringen.

#### Sprache ermöglicht alles
KI konnte früher schon vor LLM's Aufgaben für uns Menschen lösen, besser und schneller als es für uns Möglichst ist. Allerdings sind dies KI's immer genau auf Ihr Problem abgestimmt und das erzeugt Modell kann oft bis gar nicht auf andere Probleme übertragen werden. Ist z.B. ein Modell darauf trainiert Schäden an Leihwagen zu erkennen, um die Abnahme zu automatisieren, kann dieses Modell eben nur genau das. Es kann nicht Schäden an Mehrweg-Glasflaschen für die Wiederbefüllung erkennen, das wiederum benötigt ein erneutes Training mit komplett anderen Daten.

Bei natürlicher Sprache verhält es sich ähnlich, LLM's die auf Sprache trainiert sind können wiederum keine Schäden an Mehrweg-Glasflaschen erkennen. Allerdings ist natürliche Sprache die Schnittstelle von uns Menschen untereinander. Sobald man natürliche Sprache verarbeiten kann, kann man mit jedem Menschen der die gleiche Sprache spricht interagieren. Und Sprache ermöglicht den Zugang zu all dem Wissen, Regeln und Dramen die wir Menschen aufgeschrieben haben, ohne die Daten speziell für die Verarbeitung aufbereiten zu müssen.

Genau das macht LLM's so mächtig, sie können Daten (Text) verarbeiten ohne das Techniker diese filtern oder vorbereiten müssen, es fällt enorm viel Aufwand und somit Kosten weg die sonst andere Systeme in anderen Bereichen mit sich bringen. Außerdem können LLM's, dank Ihrem erlernten Allgemeinwissen, ohne jegliche Anpassung an auf verschiedenste und sogar dynamische Probleme angesetzt werden.



#### AI-Agenten & Tools
Sprachmodelle sind nicht nur auf natürliche Sprache limitiert, denn unsere Informationssysteme wie Server, Datenbanken und Webseiten werden durch Sprache und Text gesteuert und definiert. LLM's sind genauso gut in der Lage Code zu verstehen und wieder auszugeben, was eine weitere Dimension eröffnet. LLm's können Server administrieren, Sie können selbständig Emails versenden oder auch eine kleine Homepage programmieren, einfach nur durch die Eingabe von unseren Wünschen.

D.h. das Chat-Fenster von ChatGPT ist nur die Spitze des Eisberges. Das man mit einer Chateingabe auf einmal ganze PowerPoint-Präsentationen generieren kann ist nicht wirklich magisch oder technisch ausgefeilt. Die Modelle dahinter wurden darauf nachtrainiert die Schnittstellen die es für Programmiere eh schon gab nun auch bedienen zu können.

Außerdem muss die Eingabe für ein Sprachmodell nicht immer von einem Menschen kommen. Die Eingabe kann wiederum durch andere Systeme automatisiert werden, z.B. beim Eingang einer neuen Email kann diese automatisch an ein LLM übergeben werden das den Inhalt analysiert. Weiter gedacht können so mehrere LLM's miteinander arbeiten, so das die Ausgabe des einen Sprachmodells die Eingabe für das nächste Model ist, ähnlich wie eine Mitarbeiterstruktur in einer Firma bei der jeder Mitarbeiter seine abgegrenzte Aufgabe hat.



#### Limits, Halluzinationen & Zensur
Es kann immer wieder mal Vorkommen das LLM's falsche Ausgaben generieren also Lügen oder Fakten glaubhaft zu verdrehen. Auf Code der von LLM's erzeugt werden funktioniert nicht immer auf anhieb. Solche Fehler nennt man Halluzinationen. Wie bereits ganz am Anfang erwähnt geben alle ML-Algorithmen nur eine Schätzung für eine Problemstellung hab und das gilt nach wie vor auch für LLM's. Was zwangsläufig bedeutet das LLM's nicht fehlerfrei sein können, auch wenn diese stetig verbessert werden. LLMs sind darauf trainiert da nächste Wahrscheinliche Token vorherzusagen, eine Inhaltliche Prüfung auf Wahrheit oder Logik gibt es innerhalb eines Sprachmodel nicht.

![Je kleiner ein Modell desto schlechter seine Antworten. Hier wurde ein extrem kleines Model verwendet und Halluzinationen zu veranschaulichen](./mat/3.cencored.png)

Für LLM's existieren keine Regelungen oder Standards auf welchen Daten trainiert wird, das gleiche gilt für das Fine-Tuning das verhindert das Modelle Gewalt oder Kriminalität unterstützen. D.h. wir haben keinen bis kaum Einblick darauf wie neutral die Modelle der großen KI-Firmen sind. Und auch wissen wir nicht ob Ideologische Ideen und Gesellschaftliche Werte hineingeflossen sind. Ein Beispiel an dem das gut Sichtbar wird ist wenn man Chinesische Modelle nach dem "Tian'anmen-Massaker" Fragen, diese geben darauf keine Antwort. D.h. heißt das Firmen und Staaten die absolute Hoheit über diese Sprachmodelle haben. Auch können Sicherheitsmaßnamen hinderlich sein wenn es gerade um die Forschung von kritischen Themen geht, wie z.B. die Erforschung und Wirkung von Drogen.

![Das chinesische Modell 'Qwen3 8B' gibt keine Antworten zu china-kritischen Fragen.](./mat/3.cencored.png)



#### Rechenzentren und Atomkraftwerke
Die Verarbeitung und Generierung von Sprachmodellen erfordert immense Rechenleistung und damit verbunden auch eine enorme Menge an Strom. Das Training eines großen Sprachmodells wie GPT-3 kann Tage dauern und kostet mehrere Millionen Dollar, hauptsächlich aufgrund der Energiekosten für die Betrieb der Rechenzentren. Aber nicht nur das Training sondern auch die Ausführung von Sprachmodellen erfordert eine immense Leistung, was ebenfalls zu hohen Energieverbräuchen führt.

![Alle Computer und Server lassen sich durch Textbefehle steuern, und dadurch könnten LLM's diese auch theoretisch administrieren.](./mat/3.ps.png)

Einige große Technologieunternehmen haben in den letzten Jahren begonnen, ihre Datenzentren mit erneuerbaren Energien wie Solar- und Windkraft zu versorgen, um ihre CO2-Emissionen zu reduzieren. Allerdings ist der Bedarf an Strom für KI-Anwendungen so groß, dass selbst ein vollständiger Wechsel auf erneuerbare Energiequellen nicht ausreicht, um die wachsende Nachfrage zu decken.


![Ein Atomkraftwerk nur für LLM's.](./mat/3.Atom.png)

Einige Experten argumentieren sogar, dass der Stromverbrauch von KI-Anwendungen in Zukunft so hoch sein könnte, dass er den Bedarf an elektrischer Energie insgesamt beeinflussen könnte. In der Tat hat das US-Energieministerium in einer Studie festgestellt, dass der Stromverbrauch für KI-Anwendungen bis 2025 um das Zehnfache steigen könnte.

Insgesamt ist die Energieversorgung für KI-Anwendungen ein komplexes Thema, das politische, wirtschaftliche und technische Aspekte umfasst. Es bleibt abzuwarten, wie sich dieser Sektor in den kommenden Jahren entwickeln wird und welche Lösungen gefunden werden, um die wachsende Nachfrage nach Strom zu decken, während gleichzeitig die Umweltauswirkungen minimiert werden.
