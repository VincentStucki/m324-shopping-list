# Reflexion

## Einzelne Schritte 

### Aufgabe 1

Als aller Erstes habe ich ein Repo erstellt und den git folder gelöscht und die Schritte gemacht, um es in meinem Repo zu pushen.
Dann erstellte ich die folders im root: .github/workflows und dort die Datei ci.yml und habe erneut gepushed.


### Aufgabe 2

Hier habe ich angefangen einzelne Strukturen aus meinen voherigen Refcard zu übernehmen z.b. das mit dem push auf main und jobs, steps. Dann habe ich die Jobs lint und test erstellt mit ubuntu-22.04, da Herr Lanza sagte, man solle nicht latest benutzen.
Ich habe dann die Steps erstellt, um die Linting und Testing zu machen. Dies kopierte ich stück für stück aus meinem Refcard. Das habe ich gepushed und habe bemerkt das test failed ist und bemerkte das im package.json kein **test: "jest"** entählt (dank chatgpt).

### Aufgabe 3

Ja, was soll ich sagen, deployment erstellt, zwar nicht mit Docker oder so, sondern mit echo.

## Add-ons

- needs habe ich hinzugefügt, da sonst alles parallelveräuft, was nicht geschehen sollte. Vor allem beim deployment. Lintin und Testing kann parallel laufen, was im PDF mal stand beim 13.1 Pipline Optimieren aber habe es trotzdem nacheinander gemacht.
- node-version habe ich auch festgellegt da latest nie gut ist (Zitat von Herr Lanza).

## Kritik

Es ist keine fertige Github Action. 
- Man könnte ein Dockerfile erstellen und automatisch nach dem pushen ein docker image erstellen.
- Man sollte **needs** benutzen
- Wenn schon richtiges deployment dann auch ein build job
- Falls man das Projekt in mehreren Umgebungen testen möchte, kann man **matrix** benutzen
- Man soll in package.json ein jtest hinzufügen
