# Java und Listen

Listen brauchen wir häufig, wenn wir nicht eine Menge von einzelnen Variablen anlegen wollen und viele Variablen mit dem gleichen Datentyp abspeichern wollen.

Beispiel: Die Noten einer Schulklasse als integer Variable können wir so anlegen:

```
int note1 = 2;
int note2 = 4;
int note3 = 1;
...
```
Das Problem damit ist der Zugriff. Angenommen wir wollen jetzt einen Notendurchschnitt errechnen, dann müssen wir alle Noten zusammenzählen und durch die Anzahl der Noten teilen:

`float durchschnitt = (note1+note2+note3)/3;`

Wenn jetzt eine Note dazukommt, müssen wir auch unseren Programmcode zum Durchschnitt ändern.

## Java Collections Bibliothek

Java gibt uns ganz tolle Werkzeuge. Andere Leute haben Javacode geschrieben der es uns einfach macht Listen zu erstellen und zu verwenden. Solchen Code den andere Leute geschrieben haben und mitgeliefert wird bezeichnen wir als Bibliothek. Wir können uns dort Bücher also Funktionen, Klassen ausleihen und in unserem eigenen Programmcode verwenden.

Ihr habt das sicher schonmal gemacht. Zum Beispiel mit [java.swing](https://docs.oracle.com/javase/7/docs/api/javax/swing/package-summary.html) kommen diese ganzen JFrame, Jpanel, J... Klassen. Wir reden dann von der swing Bibliothek.

[Es gibt noch viel mehr Bibliotheken](https://docs.oracle.com/javase/7/docs/api/overview-summary.html) in Java. Eine davon brauchen wir jetzt. [java.util](https://docs.oracle.com/javase/7/docs/api/java/util/package-summary.html) ist die sogenannte Collections Bibliothek.

## List

`List` ist das Schlüsselwort mit dem wir eine neue Liste erstellen können:
`List meineListe = new ArrayList();`

Wieso jetzt `ArrayList()`? `List` ist leider keine Klasse, sondern ein Interface. Das soll uns jetzt nicht weiter stören. Wir können es auf der "linken Seite" unserer Variablendeklaration aber genauso wie eine Klasse verwenden. "Rechts vom Gleichheitszeichen" steht mit `ArrayList` ein Klassenname so wie wir das auch von z.B. `new Jpanel()`kennen.

List hat eine Menge toller Methoden die wir verwenden können. Zum Beispiel kennen wir schon die `size()` Methode, die uns die Anzahl der Elemente in der Liste gibt.

>Wiederholung:
>
>Methoden werden immer mit einem Punkt auf unseren Variablen aufgerufen `meineListe.size()`.

Wichtig für uns sind:

1. `size()`  
Anzahl der Elemente in der Liste.
2. `add(neuesElement)`  
neues Element an das Ende der Liste anhängen.
3. `add(index, neuesElement)`  
neues Element an einer bestimmten Stelle einfügen und alle Elemente danach nach unten schieben.
4. `addAll(eineAndereListe)`  
eine andere Liste dieser Liste hinzufügen.
5. `addAll(index, eineAndereListe)`  
eine andere Liste an einer bestimmten Stelle dieser Liste hinzufügen, alle Elemente nach dieser Stelle werden entsprechend nach unten verschoben.
6. `get(index)`  
gibt das Element an einer bestimmten Stelle zurück.
7. `remove(index)`  
Element an einer bestimmt Stelle entfernen, alle Elemente danach rutschen eines nach oben.
8. `removeAll(eineAndereListe)`  
Entfernt alle Elemente die in der anderen Liste sind aus dieser Elemente.
9. `set(index, geaendertesElement)`  
Ersetzt ein Element an einer bestimmten Stelle durch ein geaendertesElement.

[Nachzulesen auch hier.](https://docs.oracle.com/javase/7/docs/api/java/util/List.html)

## Code für alle Elemente in der Liste

Wenn wir Listen haben kann es passieren, dass wir für jedes Element einer Liste den selben Code ausführen wollen. Z.B. wir wollen alle Elemente auf der Konsole anzeigen.

Dafür können wir for-Schleifen so verwenden:

```
List meineListe = new ArrayList();
meineListe.add("Hallo");
meineListe.add("Welt");

for (String listenElement : meineListe) {
  System.out.println(listenElement);
}
```

Hierbei steht in der Klammer nach dem for
1. Der Typ unserer Listenelemente (int, String, Vokabel, ...)
2. ein neuer lokaler Variablenname, der nur für diese Schleife gilt
3. : (Doppelpunkt)
4. Der Name der Listenvariable.

## Aufgabe

Mit diesem Wissen kannst du das Beispiel vom Anfang mit den Noten als Liste aufschreiben.
