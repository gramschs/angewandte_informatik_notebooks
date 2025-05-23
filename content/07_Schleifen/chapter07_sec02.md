---
jupytext:
  formats: ipynb,md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.13.8
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# 7.2 Schleifen mit Bedingung (while)

Ein typisches Beispiel aus dem Alltag, bei dem wir etwas wiederholen, solange
eine Bedingung erfüllt ist, ist das Kochen von Wasser. Moderne Wasserkocher
haben einen eingebauten Temperatursensor, der die Temperatur des Wassers misst.
Solange die Wassertemperatur kleiner als 100 ˚C ist, wird das Wasser
erhitzt. Sobald die 100 ˚C erreicht sind, wird der Wasserkocher
abgeschaltet. Solche Wiederholungen wollen wir nun mit Python umsetzen.

## Lernziele

* Sie können eine Schleife mit Bedingung als **while**-Schleife in Python
  implementieren.
* Sie können mit **break** eine Schleife vorzeitig abbrechen.
* Sie können mit **continue** eine Schleife vorzeitig fortsetzen.

## Syntax der while-Schleife

Bei einer Wiederholung mit Bedingung werden eine oder mehrere Anweisungen
solange wiederholt, wie die Bedingung erfüllt ist. Die sogenannte while-Schleife
hat folgende Struktur:

```python
 while Bedingung: 
        anweisungsblock
```

Die bedingte Wiederholung wird mit dem Schlüsselwort `while` eingeleitet. Dann
folgt die Bedingung, die mit einem `:` abgeschlossen wird. Alle Anweisungen, die
wiederholt werden sollen, werden eingerückt. Diesen Teil nennt man das
Schleifeninnere, die Zeile `while Bedingung:` nennt man den Schleifenkopf.

**Warnung:**
While-Schleifen sind ein mächtiges Werkzeug in Python, aber es ist wichtig, sie
sorgfältig zu verwenden. Eine schlecht definierte Bedingung könnte dazu führen,
dass die Schleife **unendlich** läuft, was zu Problemen führen kann.

Um auf das Beispiel mit dem Wasserkocher zurückzukommen ... auch wenn wir jetzt
keinen echten Temperatursensor haben, würde eine while-Schleife

```{code-cell} ipython3
temperatur = 20
while temperatur <= 100:
  print(f'aktuelle Wassertemperatur: {temperatur} ˚C')
  temperatur += 10 
print('Befehl an Wasserkocher: schalte das Heizelement aus!')
print('Das Wasser ist fertig gekocht!')
```

**Mini-Übung**
Schreiben Sie ein Programm, das einen Countdown von 10 nach 0 implementiert.

```{code-cell} ipython
# Hier Ihr Code
```

## Schleifen abbrechen mit break

Die `break`-Anweisung kann verwendet werden, um die Schleife vorzeitig zu
beenden, auch wenn die Bedingung der `while`-Schleife noch `True` ist. Hier ist
ein Beispiel:

```{code-cell} ipython
zaehler = 0
while zaehler < 5:
    if zaehler == 3:
        break
    print(f'Der Zaehler hat aktuell den Wert: {zaehler}.')
    zaehler = zaehler + 1
```

**Mini-Übung**
Schreiben Sie ein Programm, das vom Benutzer natürliche Zahlen abfragt und diese
quadriert und ausgibt. Wird eine 0 eingegeben, soll die Eingabe der Zahlen
abgebrochen werden und die Meldung "Sie haben 0 eingegeben, das Programm wird
beendet." ausgegeben werden.

```{code-cell} ipython3
# Hier Ihr Code
```

## Schleifen vorzeitig fortsetzen mit continue

Die `continue`-Anweisung wird verwendet, um den aktuellen Durchgang der Schleife
zu beenden und sofort mit dem nächsten Schleifendurchgang zu beginnen. Hier ist
ein Beispiel:

```{code-cell} ipython
zaehler = 0
while zaehler < 5:
    zaehler = zaehler + 1
    if zaehler == 3:
        continue
    print(f'Der Zaehler hat aktuell den Wert: {zaehler}.')
```

In diesem Beispiel wird "Der Zaehler hat aktuell den Wert: 3" nicht ausgegeben,
da die `continue`-Anweisung dafür sorgt, dass vorzeitig der nächste
Schleifendurchgang begonnen wird, sobald `zaehler` den Wert `3` erreicht.

**Mini-Übung**
Schreiben Sie ein Programm, das eine Zahl abfragt und deren Wurzel berechnet
und ausgibt. Wird eine negative Zahl eingegeben, so soll die Wurzelberechnung
übersprungen werden. Insgesamt soll das Programm solange laufen, bis drei
Wurzeln berechnet wurden.

```{code-cell} ipython3
# Hier Ihr Code
```

## Zusammenfassung und Ausblick

Von den Schleifen kommen wir im nächsten Kapitel zu einem komplett anderem
Thema: Dictionaries.
